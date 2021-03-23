---
description: 瓷磚灌漿的顏色和厚度。 模擬陶瓷和天然石磚的灌漿。
seo-description: 瓷磚灌漿的顏色和厚度。 模擬陶瓷和天然石磚的灌漿。
seo-title: 灌漿
solution: Experience Manager
title: 灌漿
uuid: 00069004-40f2-4ab6-85d8-ca197b7bef69
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 2%

---


# 灌漿劑{#grout}

瓷磚灌漿的顏色和厚度。 模擬陶瓷和天然石磚的灌漿。

grout= *`color`*[,*`width`*]

<table id="simpletable_302B78CFC8F14E0F962D1D2064AD1371"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 顏色  </span> </span> </p> </td> 
  <td class="stentry"> <p>灌漿顏色（灰色或RGB）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> width </span> </span> </p> </td> 
  <td class="stentry"> <p>灌漿厚度；場景坐標單位（通常為英吋）（實數）。 </p> </td> 
 </tr> 
</table>

為了最大限度地控制灌漿外觀，應滿足以下要求：

* 瓷磚必須是正方形或矩形；目前不支援其他形狀。
* 影像只能包含單一圖格。
* 影像中的預設灌漿（如果有的話）在所有四條邊緣上必須具有完全相同的厚度。
* 預設灌漿的厚度必須在材料目錄(`catalog::GroutWidth`)中指定。

## 屬性 {#section-de78b678245b4ffda48097c345949e77}

材料屬性。 `*`顏`*` 色必須是RGB顏色值。`*`Width`*` 必須是實際值0或更大。

如果重複= 4、5、7、8、9、14或更高，或指定用於可重複紋理以外的材質時，則忽略。

## 預設 {#section-bfab3621f70b4489a21994ab11b20cc6}

如果未指定`grout=`，則不會修改影像中的灌漿。 如果指定` grout= *`color`*`，則`*`width`*`預設為`catalog::GroutWidth`。

## 另請參閱 {#section-8d472906a44943f5a8557e98f2fbc71f}

[顏色值](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/r-ir-color-values.md#reference-657f95c0841742d2a55a48bc938303f6)
