---
description: 替代變數可用來將值從請求URL傳輸至複合影像目錄中儲存的範本。 變數也可用來將相同的值傳達給複雜請求中的不同位置。
solution: Experience Manager
title: 替代變數
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 9fd73d16-e8bd-4fdb-a4e6-e86e5d219114
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '735'
ht-degree: 0%

---

# 替代變數{#substitution-variables}

替代變數可用來將值從請求URL傳輸至複合影像目錄中儲存的範本。 變數也可用來將相同的值傳達給複雜請求中的不同位置。

` $ *``*= *`varvalue`*`

<table id="simpletable_EFEC66C23CE949EFACDC415A954DF323"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var  </span> </span> </p> </td> 
  <td class="stentry"> <p>變數名稱。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> value  </span> </span> </p> </td> 
  <td class="stentry"> <p>變數要設定的值（字串）。 </p> </td> 
 </tr> 
</table>

變數定義和參考可能發生在請求的查詢部分、`catalog::Modifier`和`catalog::PostModifier`中。

變數定義如上，與其他IS命令類似；前導「$」將命令標識為變數定義。 必須先定義變數，才能參考。

變數名稱&#x200B;*`var`*&#x200B;不區分大小寫，並且可能包含ASCII字母、數字、「 — 」、「_」和「。」的任意組合。

>[!NOTE]
>
>*`value`* 必須採用單通URL編碼，才能安全HTTP傳輸。如果透過HTTP重新傳輸&#x200B;*`value`*，則需要雙重編碼。 在&#x200B;*`value`*&#x200B;被替換成嵌套的外部請求或SVG `<image>`元素的href屬性時，即是如此。

變數參考包含由前置和尾端「$」($*var*$)分隔的變數名稱。 任何IS命令的值部分中都可能出現引用（即，在命令名後的「=」與後續的「&amp;」或請求的結尾之間）。 無法將自定義變數應用於`layer=`和`effect=`命令。 同一命令值中允許多個變數。 伺服器會將每次出現的` $ *`var`*$`替換為&#x200B;*`value`*。

變數引用不能巢狀。 *`value`*&#x200B;內` $ *`var`*$`的任何出現次數均未取代。

例如，請求片段：

`$var2=apple&$var1=my$var2$tree&text=$var1$`

解析為：

`text=my$var2$tree`

>[!NOTE]
>
>「$」不是保留字元；若非如此，則可能發生在要求中。 例如，`src=my$image$file.tif`是有效命令（假設存在名為`my$image$file.tif`的目錄條目或影像檔案），而`wid=$number$`則否，因為`wid`需要數字參數。

## 巢狀請求中的變數處理 {#section-26d63adc446c4fa0808e11e8082abdfa}

` $ *``*$` 變數參考可能會發生在巢狀影像提供或影像呈現請求的大括弧內的任何位置，包括「？」左側將路徑與查詢分開。 在進一步剖析和處理巢狀請求之前，伺服器會以值（來自URL或來自主影像目錄的`catalog::Modifier`）取代這些參考。

此外，URL或`catalog::Modifier`中的所有` $ *`var`*=`定義都會轉送至所有巢狀的「影像伺服」和「影像呈現」請求。 這可確保所有變數定義都可供所有範本使用，無論巢狀層級為何。

無論巢狀層級為何，只能將單通HTTP編碼套用至要在巢狀影像呈現或影像伺服請求或其相關聯`catalog::Modifier`字串中任何位置取代的變數值。

## 內嵌外掛程式請求中的變數處理 {#section-314e39a9aefb46faa737fd137897d1b0}

` $ *``*$` 內嵌外掛程式請求的大括弧內任何位置出現的變數參考，都會取代為相符的變數定義值。這可讓內嵌的外來請求放置在影像目錄的範本中。

要替換為外部請求的變數值通常必須經過雙重編碼，因為在伺服器嘗試傳輸最終的外部URL之前，不會應用重新編碼。

## SVG檔案中的變數處理 {#section-a8359f9909764142b6a18ae778dca913}

` $ *``*$` varreferences可能發生在SVG檔案中的屬性值和字 `<text>` 串中。「影像伺服」會以在指定SVG檔案的請求巢狀層級已知的相符` $ *`var`*=`定義來取代這些定義。

>[!NOTE]
>
>任何要替換為`href`屬性值的變數值都必須經過雙重URL編碼；所有其他的都必須單獨編碼。

## 預先定義的路徑變數 {#section-930d0dd12e8f49499becc9fe8df24092}

在請求路徑中指定的&#x200B;*`object`*&#x200B;會指派給預先定義的變數`*`$object`*`。 「 ` $ *`object`*$`」可放置在請求中、請求引用的模板中或允許此類對象的嵌套/嵌入請求中的任意位置，包括`src=`和`mask=`的值，以及嵌套/嵌入請求的路徑。

例如，下列請求會重複使用路徑中指定的影像，作為巢狀請求中層的來源：

`/is/image/a/b?…&layer=3&src=is{…&src=$object$}&…`

這等同於

`/is/image/a/b?…&layer=3&src=is{…&src=a/b}&…`

可以顯式指定` $ *`object`*=`並指定所需值來覆蓋`*`$object`*`的定義。

預先定義的路徑變數通常與`template=`搭配使用。

## 預設 {#section-b02483d15529444586a2e9504805b155}

無. 只有已定義的變數才會被伺服器取代（預先定義的路徑變數$object除外，它們一律會被取代）。 如果`*`var`*`無法與現有變數定義相符，則` $ *`var`*$`的任何出現次數都會保持常值。

## 範例 {#section-fba9393df6984247b7e30b3f93992e86}

請參閱[範本](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)中的「範例A」。

## 另請參閱 {#section-11b44cc824744f70b1705ebdd9ec4fe6}

[範本](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e), [範本=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-template.md#reference-3beccaa462a64bf0ba867e5c8fd0bd14)
