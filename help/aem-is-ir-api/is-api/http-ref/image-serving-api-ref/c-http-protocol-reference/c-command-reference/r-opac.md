---
description: 調整影像不透明度。 允許降低影像、文本、實色或效果層的前景不透明度。
solution: Experience Manager
title: opac
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 38e0e1dc-46c0-48a4-b676-f7e6d262392f
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 2%

---

# opac{#opac}

調整影像不透明度。 允許降低影像、文本、實色或效果層的前景不透明度。

`opac= *``*[, *`opacityfillOpacity`*]`

<table id="simpletable_DA4B5D86C496480886FADB284AD6047F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 不透明度</span> </p> </td> 
  <td class="stentry"> <p>主不透明度（0...100整）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> fillOpacity</span> </p></td> 
  <td class="stentry"> <p>填充不透明度（0...100整）。 </p></td> 
 </tr> 
</table>

影像層的前景不透明度由圖層遮色片或影像的α通道確定，或者，如果兩者均不存在，則為100%。 文本層的前景不透明度為100%，而實色層的前景不透明度由`color=`設定。

`opac=` 除了實色和效果圖層的前 `color=` 景區域(以 `bgColor=`設定)外，絕不修改或填充區域的不透明度 `color=`。

當在影像、文本或實色層中指定時，*`opacity`*&#x200B;應用整個層，包括所有相關的效果層，而&#x200B;*`fillOpacity`*&#x200B;僅應用於主層內容。 在效果層中指定時， *`opacity`*&#x200B;將應用於效果層，而忽略&#x200B;*`fillOpacity`*。

主層內容的有效不透明度為(*`opacity`* * *`fillOpacity`* / 100)。 有效不透明度為（主&#x200B;*`opacity`* *效應&#x200B;*`opacity`* / 100）。

## 屬性 {#section-ac3f136ff1584a2eab87500b7164f7fa}

層屬性。 若`layer=comp`，則套用至目前層或複合影像。

## 預設 {#section-abba67ed028049048ae43405ea69b164}

`opac=100,100`，不會更改圖層不透明度。

## 範例 {#section-9710810e96af40538652e8ae4aadd3be}

… `&layer=1&text=variable%20opacity&opac=90,70&effect=-1&opac=50&`…

此示例中的文本不透明度為90*70/100=63%，效果層不透明度為90*50/100=45%。

## 另請參閱 {#section-dbdad35ccd544590b4b11d31a9ab062e}

[color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) ,  [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab)
