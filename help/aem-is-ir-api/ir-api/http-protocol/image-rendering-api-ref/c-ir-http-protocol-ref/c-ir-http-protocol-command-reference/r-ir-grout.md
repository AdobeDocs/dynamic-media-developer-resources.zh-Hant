---
description: 瓷磚灌漿的顏色和厚度。 模擬陶瓷和天然石磚的灌漿。
solution: Experience Manager
title: 灌漿
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6647b459-11d2-47e4-9033-3a740f01a623
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 2%

---

# 灌漿{#grout}

瓷磚灌漿的顏色和厚度。 模擬陶瓷和天然石磚的灌漿。

grout= *`color`*[,*`width`*]

<table id="simpletable_302B78CFC8F14E0F962D1D2064AD1371"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 色彩  </span> </span> </p> </td> 
  <td class="stentry"> <p>灌漿顏色（灰色或RGB）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> width </span> </span> </p> </td> 
  <td class="stentry"> <p>灌漿厚度；場景坐標單位（通常為英吋）（實數）。 </p> </td> 
 </tr> 
</table>

為了最大限度地控制灌漿外觀，應滿足以下要求：

* 瓷磚必須是正方形或矩形；目前不支援其他形狀。
* 影像只能包含單一圖磚。
* 影像中的預設灌漿（如果有）在所有四條邊上必須具有相同的厚度。
* 必須在材料目錄(`catalog::GroutWidth`)中指定預設漿液的厚度。

## 屬性 {#section-de78b678245b4ffda48097c345949e77}

材料屬性。 `*``*` color必須是RGB顏色值。`*``*` width必須是實際值0或更大。

如果重複= 4、5、7、8、9、14或更高，或為可重複紋理以外的材料指定時，則忽略。

## 預設 {#section-bfab3621f70b4489a21994ab11b20cc6}

如果未指定`grout=`，則不修改影像中的灌漿。 如果指定` grout= *`color`*`，則`*`width`*`預設為`catalog::GroutWidth`。

## 另請參閱 {#section-8d472906a44943f5a8557e98f2fbc71f}

[顏色值](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/r-ir-color-values.md#reference-657f95c0841742d2a55a48bc938303f6)
