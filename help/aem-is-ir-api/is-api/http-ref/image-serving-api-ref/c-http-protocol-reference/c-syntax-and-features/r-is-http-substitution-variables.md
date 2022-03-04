---
description: 替換變數用於將值從請求URL傳輸到儲存在影像目錄中的合成模板。 變數還可用於將相同值傳遞到複雜請求中的不同位置。
solution: Experience Manager
title: 替代變數
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9fd73d16-e8bd-4fdb-a4e6-e86e5d219114
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '729'
ht-degree: 0%

---

# 替代變數{#substitution-variables}

替換變數用於將值從請求URL傳輸到儲存在影像目錄中的合成模板。 變數還可用於將相同值傳遞到複雜請求中的不同位置。

` $ *`var`*= *`值`*`

<table id="simpletable_EFEC66C23CE949EFACDC415A954DF323"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var </span> </span> </p> </td> 
  <td class="stentry"> <p>變數名稱。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 值 </span> </span> </p> </td> 
  <td class="stentry"> <p>要設定變數的值（字串）。 </p> </td> 
 </tr> 
</table>

變數定義和引用可能發生在請求的查詢部分，在 `catalog::Modifier`中 `catalog::PostModifier`。

變數定義如上，與其他IS命令類似；前導「$」將命令標識為變數定義。 在引用變數之前必須定義變數。

變數名稱 *`var`* 不區分大小寫，並且可能包含ASCII字母、數字、「 — 」、「_」和「。」的任意組合。

>[!NOTE]
>
>*`value`* 必須是單通URL編碼，才能進行安全的HTTP傳輸。 如果需要雙重編碼， *`value`* 通過HTTP重新傳輸。 這就是 *`value`* 替換為嵌套的外部請求或SVG的href屬性 `<image>` 的子菜單。

變數引用由前導和尾隨「$」($)分隔的變數名稱組成&#x200B;*var*$)。 任何IS命令的值部分（即，在命令名稱后的「=」與隨後的「&amp;」或請求的結束之間）的任何位置都可能出現引用。 自定義變數無法應用到 `layer=` 和 `effect=` 的雙曲餘切值。 同一命令值中允許多個變數。 伺服器替換了 ` $ *`var`*$` 與 *`value`*。

變數引用不能嵌套。 任何出現的 ` $ *`var`*$` 內 *`value`* 的下界。

例如，請求片段：

`$var2=apple&$var1=my$var2$tree&text=$var1$`

解析為：

`text=my$var2$tree`

>[!NOTE]
>
>「$」不是保留字元；在請求中可能會出現其它情況。 比如說， `src=my$image$file.tif` 是有效命令(假定名為 `my$image$file.tif` 存在)，而 `wid=$number$` 不是，因為 `wid` 需要一個數字參數。

## 嵌套請求中的變數處理 {#section-26d63adc446c4fa0808e11e8082abdfa}

` $ *`var`*$` 引用可能發生在嵌套的Image Serving或Image Rendering請求的大括弧內的任何位置，包括「？」左側 將路徑與查詢分離。 伺服器用值替換這些引用(從url或從 `catalog::Modifier` 在進一步解析和處理嵌套請求之前，對所述主影像目錄（如主影像目錄）進行解析和處理。

另外， ` $ *`var`*=` 定義 `catalog::Modifier` 轉發到所有嵌套的Image Service和Image Rendering請求。 這可確保所有變數定義都可用於所有模板，而不管嵌套級別如何。

無論嵌套級別如何，只能將單遍HTTP編碼應用於要在嵌套的影像呈現或影像服務請求或其關聯的任何位置替換的變數值 `catalog::Modifier` 字串。

## 嵌入式外部請求中的變數處理 {#section-314e39a9aefb46faa737fd137897d1b0}

` $ *`var`*$` 在嵌入的外部請求的大括弧內出現的引用將替換為匹配的變數定義值。 這允許將嵌入的外來請求放置在影像目錄中的模板中。

要替換為外部請求的變數值通常必須是雙編碼的，因為在伺服器嘗試傳輸最終的外部url之前不應用重新編碼。

## 在SVG檔案中進行變數處理 {#section-a8359f9909764142b6a18ae778dca913}

` $ *`var`*$` 在屬性值和中的SVG檔案中可能出現引用 `<text>` 字串。 影像服務用匹配替換這些 ` $ *`var`*=` 在指定SVG檔案的請求嵌套級別已知的定義。

>[!NOTE]
>
>要替換為 `href` 屬性值必須是雙URL編碼；所有其它內容必須單獨編碼。

## 預定義路徑變數 {#section-930d0dd12e8f49499becc9fe8df24092}

的 *`object`* 在請求路徑中指定的變數被分配給預定義的變數 `*`$object`*`。 &quot; ` $ *`對象`*$`「可以放置在請求、請求引用的模板或允許此對象的嵌套/嵌入請求中的任何位置，包括 `src=` 和 `mask=`，以及嵌套/嵌入式請求的路徑。

例如，以下請求將重用路徑中指定的影像作為嵌套請求中層的源：

`/is/image/a/b?…&layer=3&src=is{…&src=$object$}&…`

這相當於

`/is/image/a/b?…&layer=3&src=is{…&src=a/b}&…`

定義 `*`$object`*` 可以通過顯式指定 ` $ *`對象`*=` 值。

預定義路徑變數通常與 `template=`。

## 預設 {#section-b02483d15529444586a2e9504805b155}

無. 只有已定義的變數被伺服器替換（預定義的路徑變數$object除外，它將始終被替換）。 任何出現的 ` $ *`var`*$` 如果 `*`var`*`無法與現有變數定義匹配。

## 範例 {#section-fba9393df6984247b7e30b3f93992e86}

請參閱中的「示例A」 [模板](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)。

## 另請參閱 {#section-11b44cc824744f70b1705ebdd9ec4fe6}

[模板](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)。 [模板=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-template.md#reference-3beccaa462a64bf0ba867e5c8fd0bd14)
