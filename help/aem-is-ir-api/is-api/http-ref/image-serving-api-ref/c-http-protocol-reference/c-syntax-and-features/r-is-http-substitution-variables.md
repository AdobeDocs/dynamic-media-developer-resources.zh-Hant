---
description: 替代變數可用來將值從請求URL傳輸至影像目錄中儲存的構圖範本。 變數也可用來將相同的值傳達至複雜請求的不同位置。
seo-description: 替代變數可用來將值從請求URL傳輸至影像目錄中儲存的構圖範本。 變數也可用來將相同的值傳達至複雜請求的不同位置。
seo-title: 替代變數
solution: Experience Manager
title: 替代變數
topic: Scene7 Image Serving - Image Rendering API
uuid: e369f2c3-8d89-4169-8869-f1d7ab89aab9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 替代變數{#substitution-variables}

替代變數可用來將值從請求URL傳輸至影像目錄中儲存的構圖範本。 變數也可用來將相同的值傳達至複雜請求的不同位置。

` $ *``*= *`varvalue`*`

<table id="simpletable_EFEC66C23CE949EFACDC415A954DF323"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var </span></span> </p> </td> 
  <td class="stentry"> <p>變數名稱。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 值 <span class="varname"></span></span> </p> </td> 
  <td class="stentry"> <p>變數要設定到的值（字串）。 </p> </td> 
 </tr> 
</table>

變數定義和參考可能發生在請求的查詢部分、中 `catalog::Modifier`和中 `catalog::PostModifier`。

變數定義如下，類似於其他IS命令；前導&#39;$&#39;會將命令識別為變數定義。 變數必須先定義，才能被參考。

變數名 *`var`* 稱不區分大小寫，可能由ASCII字母、數字、&#39;-&#39;、&#39;_&#39;和&#39;.&#39;的任意組合組成。

>[!NOTE]
>
>*`value`* 必須是單次URL編碼，才能安全傳輸HTTP。 如果透過HTTP重新傳輸，則 *`value`* 需要雙重編碼。 在將其取代為 *`value`* 巢狀外部請求或SVG元素的href屬性時，即 `<image>` 為此。

變數參考包含由前導和尾隨「$」($*var*$)分隔的變數名稱。 任何IS命令的值部分中都可能出現引用（即，在命令名稱后面的&#39;=&#39;和後續的&#39;&amp;&#39;或請求結尾之間）。 自訂變數無法套用至 `layer=` 和命 `effect=` 令。 同一命令值允許使用多個變數。 伺服器會將每次出現的 ` $ *`var`*$` ，取代 *`value`*。

變數參考可能無法巢狀化。 不會取 ` $ *`代`*$`*`value`* 中的var。

例如，請求片段：

`$var2=apple&$var1=my$var2$tree&text=$var1$`

解析為：

`text=my$var2$tree`

>[!NOTE]
>
>「$」不是保留字元；在請求中可能會發生其他情況。 例如， `src=my$image$file.tif` 是有效命令（假設名為目錄條目或影像檔案存在），而 `my$image$file.tif` 不是，因為 `wid=$number$``wid` 需要數值參數。

## 巢狀請求中的變數處理 {#section-26d63adc446c4fa0808e11e8082abdfa}

` $ *`var`*$` references可能發生在巢狀「影像伺服」或「影像轉換」請求的大括弧內，包括在「?」的左側 將路徑與查詢分開。 伺服器會在進一步剖析和處理巢狀請求之前，以值( `catalog::Modifier` 來自URL或主影像目錄)來取代這些參考。

此外，URL中的 ` $ *`所有`*=` var定義或會轉送 `catalog::Modifier` 至所有巢狀的「影像伺服」和「影像演算」請求。 這可確保所有範本都可使用所有變數定義，不論巢狀層級為何。

不論巢狀層級為何，只能將單一傳遞的HTTP編碼套用至變數值，這些值將在巢狀影像演算或影像伺服請求或其相關字串中的任何位置 `catalog::Modifier` 取代。

## 內嵌外來請求中的變數處理 {#section-314e39a9aefb46faa737fd137897d1b0}

` $ *`在內嵌`*$` 外圍請求的大括弧內，隨處發生的var參考會以相符的變數定義值取代。 這允許將嵌入的外來請求放置在映像目錄的模板中。

要取代為外來請求的變數值通常必須進行雙重編碼，因為伺服器在嘗試傳輸最終外來URL之前不會套用重新編碼。

## SVG檔案中的變數處理 {#section-a8359f9909764142b6a18ae778dca913}

` $ *`var參考`*$` 可能出現在屬性值和字串中的SVG檔 `<text>` 案中。 「影像伺服」會將這些變數與指 ` $ *`定SVG檔案之請求巢狀層級已知的相符`*=` var定義取代。

>[!NOTE]
>
>任何要替換為屬性值的變 `href` 量值都必須使用雙URL編碼；所有其他項目都必須單獨編碼。

## 預先定義的路徑變數 {#section-930d0dd12e8f49499becc9fe8df24092}

請 *`object`* 求路徑中指定的值會指派給預先定義的變 ` *`數$object`*`。 「 ` $ *`object`*$`」可放置在請求中、請求引用的模板中或允許該對象的嵌套／嵌入請求中的任意位置，包括 `src=``mask=`和的值，以及嵌套／嵌入請求的路徑。

例如，下列請求會重複使用路徑中指定的影像，作為巢狀請求中圖層的來源：

`/is/image/a/b?…&layer=3&src=is{…&src=$object$}&…`

這等同於

`/is/image/a/b?…&layer=3&src=is{…&src=a/b}&…`

可以通過顯 ` *`式指定具有所需值`*` 的對象 ` $ *``*=` ，來覆蓋$object的定義。

預先定義的路徑變數通常與搭配使用 `template=`。

## 預設 {#section-b02483d15529444586a2e9504805b155}

無. 只有已定義的變數才會被伺服器取代（預先定義的路徑變數$object除外，這些變數永遠會被取代）。 如果變數不 ` $ *`能與現有變`*$` 數定義相符 ` *``*`，則任何變數的出現次數都會維持常值。

## 範例 {#section-fba9393df6984247b7e30b3f93992e86}

請參閱範本中的「範例 [A」](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)。

## 另請參閱 {#section-11b44cc824744f70b1705ebdd9ec4fe6}

[範本](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e), [範本=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-template.md#reference-3beccaa462a64bf0ba867e5c8fd0bd14)
