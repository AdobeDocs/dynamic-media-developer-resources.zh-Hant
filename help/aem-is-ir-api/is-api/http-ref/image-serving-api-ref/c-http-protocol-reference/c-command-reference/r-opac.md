---
description: 調整影像不透明度。 允許降低影像、文本、純色或效果圖層的前景不透明度。
solution: Experience Manager
title: Opac
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 38e0e1dc-46c0-48a4-b676-f7e6d262392f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 1%

---

# Opac{#opac}

調整影像不透明度。 允許降低影像、文本、純色或效果圖層的前景不透明度。

`opac= *`不透明度`*[, *`fill不透明度`*]`

<table id="simpletable_DA4B5D86C496480886FADB284AD6047F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 不透明度</span> </p> </td> 
  <td class="stentry"> <p>主不透明度(0...100 int)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> fill不透明度</span> </p></td> 
  <td class="stentry"> <p>填充不透明度(0...100 int)。 </p></td> 
 </tr> 
</table>

影像層的前景不透明度由影像的層掩模或α通道確定，或者，如果兩者都不存在，則為100%。 文本層的前景不透明度為100%，而實色層的前景不透明度由 `color=`。

`opac=` 從不修改填充區域的不透明度 `color=` 或 `bgColor=`，除了實色和效果圖層的前景區域(設定為 `color=`)。

在影像、文本或純色圖層中指定時， *`opacity`* 應用整個層，包括所有關聯的效果層，而 *`fillOpacity`* 僅適用於主層內容。 在效果層中指定時， *`opacity`* 應用於效果圖層，而 *`fillOpacity`* 忽略。

主圖層內容的有效不透明度為( *`opacity`* &#42; *`fillOpacity`* / 100)。 效果層的有效不透明度是 *`opacity`* &#42; 影響 *`opacity`* / 100)。

## 屬性 {#section-ac3f136ff1584a2eab87500b7164f7fa}

層屬性。 應用於當前圖層或複合影像 `layer=comp`。

## 預設 {#section-abba67ed028049048ae43405ea69b164}

`opac=100,100`，以保持圖層不透明度不變。

## 範例 {#section-9710810e96af40538652e8ae4aadd3be}

… `&layer=1&text=variable%20opacity&opac=90,70&effect=-1&opac=50&`…

此示例中的文本不透明度為90&#42;70/100=63%，效應層不透明度為90&#42;50/100=45%。

## 另請參閱 {#section-dbdad35ccd544590b4b11d31a9ab062e}

[顏色=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) 。 [bg顏色=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab)
