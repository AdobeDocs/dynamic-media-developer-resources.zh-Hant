---
description: 替代變數可用來將值從請求URL傳輸至影像目錄中儲存的構圖範本。 變數也可用來將相同的值傳達至複雜請求的不同位置。
solution: Experience Manager
title: 替代變數
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '738'
ht-degree: 0%

---


# 替代變數{#substitution-variables}

替代變數可用來將值從請求URL傳輸至影像目錄中儲存的構圖範本。 變數也可用來將相同的值傳達至複雜請求的不同位置。

` $ *``*= *`varvalue`*`

<table id="simpletable_EFEC66C23CE949EFACDC415A954DF323"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var  </span> </span> </p> </td> 
  <td class="stentry"> <p>變數名稱。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 值  </span> </span> </p> </td> 
  <td class="stentry"> <p>變數要設定的值（字串）。 </p> </td> 
 </tr> 
</table>

變數定義和引用可能發生在請求的查詢部分、`catalog::Modifier`和`catalog::PostModifier`中。

變數定義如下，類似於其他IS命令；前導&#39;$&#39;會將命令識別為變數定義。 變數必須先定義，才能被參考。

變數名稱&#x200B;*`var`*&#x200B;不區分大小寫，可能由ASCII字母、數字、&#39;-&#39;、&#39;_&#39;和&#39;.&#39;的任意組合組成。

>[!NOTE]
>
>*`value`* 必須是單次URL編碼，才能安全傳輸HTTP。如果&#x200B;*`value`*&#x200B;是透過HTTP重新傳輸，則需要雙重編碼。 在此情況下，*`value`*&#x200B;會取代為巢狀外來請求或SVG `<image>`元素的href屬性。

變數參考由前導和尾隨「$」($*var*$)分隔的變數名稱組成。 任何IS命令的值部分中都可能出現引用（即，在命令名稱后面的&#39;=&#39;和後續的&#39;&amp;&#39;或請求結尾之間）。 自訂變數無法套用至`layer=`和`effect=`命令。 同一命令值允許使用多個變數。 伺服器將每次出現` $ *`var`*$`的情況替換為&#x200B;*`value`*。

變數參考可能無法巢狀化。 在&#x200B;*`value`*&#x200B;內出現的` $ *`var`*$`都不會被取代。

例如，請求片段：

`$var2=apple&$var1=my$var2$tree&text=$var1$`

解析為：

`text=my$var2$tree`

>[!NOTE]
>
>「$」不是保留字元；在請求中可能會發生其他情況。 例如，`src=my$image$file.tif`是有效命令（假設存在名為`my$image$file.tif`的目錄條目或影像檔案），而`wid=$number$`則否，因為`wid`需要數字參數。

## 巢狀請求中的變數處理{#section-26d63adc446c4fa0808e11e8082abdfa}

` $ *`變`*$` 數參照可能發生在巢狀「影像伺服」或「影像轉換」請求的大括弧內，包括在「?」的左側將路徑與查詢分開。 伺服器會在進一步剖析和處理巢狀請求之前，以值（來自主影像目錄的url或`catalog::Modifier`）取代這些參考。

此外，所有來自URL或`catalog::Modifier`的` $ *`var`*=`定義都會轉送至所有巢狀的「影像伺服」和「影像演算」請求。 這可確保所有範本都可使用所有變數定義，不論巢狀層級為何。

不論巢狀層級為何，只能將單一傳遞的HTTP編碼套用至變數值，這些值將在巢狀影像演算或影像伺服請求或其相關的`catalog::Modifier`字串中的任何位置取代。

## 內嵌外來請求中的變數處理{#section-314e39a9aefb46faa737fd137897d1b0}

` $ *`在`*$` 內嵌外來請求的大括弧內，任何位置發生的變數參照都會以相符的變數定義值取代。這允許將嵌入的外來請求放置在映像目錄的模板中。

要取代為外來請求的變數值通常必須進行雙重編碼，因為伺服器在嘗試傳輸最終外來URL之前不會套用重新編碼。

## SVG檔案{#section-a8359f9909764142b6a18ae778dca913}中的變數處理

` $ *`變`*$` 量引用可能發生在屬性值和字串中的SVG `<text>` 檔案。「影像伺服」會以指定SVG檔案之請求巢狀層級已知的相符` $ *`var`*=`定義來取代這些定義。

>[!NOTE]
>
>任何要替換為`href`屬性值的變數值都必須使用雙URL編碼；所有其他項目都必須單獨編碼。

## 預先定義的路徑變數{#section-930d0dd12e8f49499becc9fe8df24092}

在請求路徑中指定的&#x200B;*`object`*&#x200B;被指派給預先定義的變數`*`$object`*`。 「 ` $ *`object`*$`」可放置在請求中的任意位置、請求引用的模板中或允許該對象的嵌套／嵌入請求中，包括`src=`和`mask=`的值，以及嵌套／嵌入請求的路徑。

例如，下列請求會重複使用路徑中指定的影像，作為巢狀請求中圖層的來源：

`/is/image/a/b?…&layer=3&src=is{…&src=$object$}&…`

這等同於

`/is/image/a/b?…&layer=3&src=is{…&src=a/b}&…`

通過顯式指定具有所需值的` $ *`object`*=`，可以覆蓋`*`$object`*`的定義。

預先定義的路徑變數通常與`template=`搭配使用。

## 預設 {#section-b02483d15529444586a2e9504805b155}

無. 只有已定義的變數才會被伺服器取代（預先定義的路徑變數$object除外，這些變數永遠會被取代）。 如果`*`var`*`無法與現有變數定義相符，則任何` $ *`var`*$`的出現次數都會維持常值。

## 範例 {#section-fba9393df6984247b7e30b3f93992e86}

請參閱[Templates](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)中的「範例A」。

## 另請參閱 {#section-11b44cc824744f70b1705ebdd9ec4fe6}

[範本](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e), [範本=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-template.md#reference-3beccaa462a64bf0ba867e5c8fd0bd14)
