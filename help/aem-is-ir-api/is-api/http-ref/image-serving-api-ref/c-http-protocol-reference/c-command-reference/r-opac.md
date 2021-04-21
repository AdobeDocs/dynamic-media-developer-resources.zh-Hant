---
description: 調整影像不透明度。 可降低影像、文字、純色或效果圖層的前景不透明度。
solution: Experience Manager
title: opac
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 2%

---


# opac{#opac}

調整影像不透明度。 可降低影像、文字、純色或效果圖層的前景不透明度。

`opac= *`不透明`*[, *`度填滿不透明度`*]`

<table id="simpletable_DA4B5D86C496480886FADB284AD6047F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 不透明度</span> </p> </td> 
  <td class="stentry"> <p>主要不透明度(0...100 int)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> fillOpacity</span> </p></td> 
  <td class="stentry"> <p>填滿不透明度(0...100 int)。 </p></td> 
 </tr> 
</table>

影像層的前景不透明度由圖層遮色片或影像的Alpha通道確定，或者，如果兩者都不存在，則為100%。 文字圖層的前景不透明度為100%，而純色圖層的前景不透明度則由`color=`設定。

`opac=` 切勿修改填入或的區 `color=` 域的不 `bgColor=`透明度，除了前景區域的純色和效果圖層(設為 `color=`)。

當在影像、文字或純色圖層中指定時，*`opacity`*&#x200B;會套用整個圖層，包括所有相關的效果圖層，而&#x200B;*`fillOpacity`*&#x200B;僅套用至主要圖層內容。 當在特效圖層中指定時，*`opacity`*&#x200B;會套用至特效圖層，而&#x200B;*`fillOpacity`*&#x200B;則會被忽略。

主圖層內容的有效不透明度是(*`opacity`* * *`fillOpacity`* / 100)。 效果圖層的有效不透明度是（主&#x200B;*`opacity`* *效果&#x200B;*`opacity`* / 100）。

## 屬性 {#section-ac3f136ff1584a2eab87500b7164f7fa}

層屬性。 如果`layer=comp`，則套用至目前圖層或複合影像。

## 預設 {#section-abba67ed028049048ae43405ea69b164}

`opac=100,100`，圖層不透明度不變。

## 範例 {#section-9710810e96af40538652e8ae4aadd3be}

… `&layer=1&text=variable%20opacity&opac=90,70&effect=-1&opac=50&`…

此範例中的文字不透明度為90*70/100=63%，而效果圖層不透明度為90*50/100=45%。

## 另請參閱 {#section-dbdad35ccd544590b4b11d31a9ab062e}

[color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) ,  [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab)
