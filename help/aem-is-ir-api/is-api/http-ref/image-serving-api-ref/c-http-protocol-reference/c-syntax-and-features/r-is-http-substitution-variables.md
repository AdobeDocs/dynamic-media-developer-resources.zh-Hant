---
description: 替代變數可用來將請求URL中的值傳輸到影像目錄中儲存的合成範本。 變數也可用來將相同的值傳達給複雜請求中的不同位置。
solution: Experience Manager
title: 替代變數
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9fd73d16-e8bd-4fdb-a4e6-e86e5d219114
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '736'
ht-degree: 0%

---

# 替代變數{#substitution-variables}

替代變數可用來將請求URL中的值傳輸到影像目錄中儲存的合成範本。 變數也可用來將相同的值傳達給複雜請求中的不同位置。

` $ *`var`*= *`value`*`

<table id="simpletable_EFEC66C23CE949EFACDC415A954DF323"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">變數</span> </span> </p> </td> 
  <td class="stentry"> <p>變數名稱。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">值</span> </span> </p> </td> 
  <td class="stentry"> <p>變數要設定的值（字串）。 </p> </td> 
 </tr> 
</table>

變數定義和參考可能會出現在要求的查詢部分、`catalog::Modifier`和`catalog::PostModifier`中。

變數的定義如上所述，與其他IS命令類似；前導的「$」會將該命令識別為變數定義。 必須先定義變數，才能加以參照。

變數名稱&#x200B;*`var`*&#x200B;不區分大小寫，而且可能包含ASCII字母、數字、&#39;-&#39;、&#39;_&#39;和&#39;.&#39;的任何組合。

>[!NOTE]
>
>*`value`*&#x200B;必須為單次URL編碼，才能安全HTTP傳輸。 若透過HTTP重新傳輸&#x200B;*`value`*，則需要雙重編碼。 當&#x200B;*`value`*&#x200B;被替換為巢狀外部請求或SVG`<image>`專案的href屬性時，就會發生這種情況。

變數參考是由開頭與結尾為「$」($*var*$)分隔的變數名稱所組成。 參考可能會出現在任何IS命令的值部分的任何位置（也就是說，在命令名稱后面的「=」和後續的「&amp;」或請求結尾之間）。 自訂變數無法套用至`layer=`和`effect=`命令。 相同命令值中允許多個變數。 伺服器會以&#x200B;*`value`*&#x200B;取代` $ *`var`*$`的每個例項。

變數參考不可使用巢狀結構。 在&#x200B;*`value`*&#x200B;內出現` $ *`var`*$`的任何專案都不會被取代。

例如，請求片段：

`$var2=apple&$var1=my$var2$tree&text=$var1$`

解析為：

`text=my$var2$tree`

>[!NOTE]
>
>「$」不是保留字元；它可能會出現在要求中的其他位置。 例如，`src=my$image$file.tif`是有效的命令（假設名為`my$image$file.tif`的目錄專案或影像檔案存在），而`wid=$number$`則否，因為`wid`需要數值引數。

## 巢狀要求中的變數處理 {#section-26d63adc446c4fa0808e11e8082abdfa}

` $ *`var`*$`參考可能會出現在巢狀影像伺服或影像演算請求的大括弧內的任何位置，包括「？」的左側 將路徑與查詢分開。 在進一步剖析及處理巢狀要求之前，伺服器會以值（來自URL或主要影像目錄的`catalog::Modifier`）取代這些參考。

此外，來自URL或`catalog::Modifier`的所有` $ *`var`*=`定義都已轉送至所有巢狀影像提供與影像轉譯請求。 這可確保所有變數定義都可供所有範本使用，無論巢狀層級為何。

無論巢狀層級為何，若要在巢狀影像演算或影像伺服要求或其相關的`catalog::Modifier`字串中的任何位置取代變數值，必須僅套用單次HTTP編碼。

## 內嵌外部請求中的變數處理 {#section-314e39a9aefb46faa737fd137897d1b0}

內嵌外部請求大括弧內任何位置出現的` $ *`var`*$`參考會被相符的變數定義值取代。 這可讓內嵌外部請求被放置在影像目錄的範本中。

要取代成外來要求的變數值通常必須經過雙重編碼，因為在伺服器嘗試傳輸最終的外部url之前不會套用重新編碼。

## SVG檔案中的變數處理 {#section-a8359f9909764142b6a18ae778dca913}

` $ *`var`*$`參考可能會出現在屬性值和`<text>`字串中的SVG檔案中。 「影像伺服」會以指定SVG檔案的請求巢狀層級已知相符的` $ *`var`*=`定義來取代這些定義。

>[!NOTE]
>
>任何要取代成`href`屬性值的變數值都必須以雙URL編碼；其他所有變數值都必須以單一編碼。

## 預先定義的路徑變數 {#section-930d0dd12e8f49499becc9fe8df24092}

要求路徑中指定的&#x200B;*`object`*&#x200B;已指派給預先定義的變數`*`$object`*`。 &#39;` $ *`物件`*$`&#39;可放置在要求中的任何位置、要求所參考的範本，或允許此類物件的巢狀/內嵌要求中，包括`src=`和`mask=`的值，以及巢狀/內嵌要求的路徑。

例如，下列要求會重複使用路徑中指定的影像，做為巢狀要求中圖層的來源：

`/is/image/a/b?…&layer=3&src=is{…&src=$object$}&…`

這相當於

`/is/image/a/b?…&layer=3&src=is{…&src=a/b}&…`

可以使用所需的值明確指定` $ *`物件`*=`，以覆寫`*`$object`*`的定義。

預先定義的路徑變數通常與`template=`搭配使用。

## 預設 {#section-b02483d15529444586a2e9504805b155}

無。 只有已定義的變數才會被伺服器取代（預先定義的路徑變數$object除外，此變數一律會被取代）。 如果`*`var`*`無法與現有變數定義比對，則` $ *`var`*$`的任何專案仍為常值。

## 範例 {#section-fba9393df6984247b7e30b3f93992e86}

請參閱[範本](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)中的「範例A」。

## 另請參閱 {#section-11b44cc824744f70b1705ebdd9ec4fe6}

[範本](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)，[範本=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-template.md#reference-3beccaa462a64bf0ba867e5c8fd0bd14)
