---
title: 灌漿
description: 瓷磚灌漿顏色和厚度。 模擬陶瓷和天然石磚的灌漿。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6647b459-11d2-47e4-9033-3a740f01a623
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 2%

---

# 灌漿 {#grout}

瓷磚灌漿顏色和厚度。 模擬陶瓷和天然石磚的灌漿。

灌漿= *`color`*[。*`width`*]

<table id="simpletable_302B78CFC8F14E0F962D1D2064AD1371"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 顏色 </span> </span> </p> </td>
  <td class="stentry"> <p>灌漿顏色(灰色或RGB)。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> width </span> </span> </p> </td>
  <td class="stentry"> <p>灌漿厚度；場景坐標單位（通常為英吋）（實數）。 </p> </td>
 </tr> 
</table>

為了最大程度地控制灌漿外觀，需要滿足以下要求：

* 瓦塊必須是方形或矩形；當前不支援其他形狀。
* 影像必須僅包含單個拼貼。
* 影像（如果有）中的預設灌漿必須在所有四條邊上具有相同的厚度。
* 預設灌漿的厚度必須在材料目錄中指定( `catalog::GroutWidth`)。

## 屬性 {#section-de78b678245b4ffda48097c345949e77}

物料屬性。 `*`顏色`*` 必須是RGB顏色值。 `*`寬度`*` 必須是實數值0或更大。

如果重複次數= 4、5、7、8、9、14或更高，或者為可重複紋理以外的材料指定時，將忽略。

## 預設 {#section-bfab3621f70b4489a21994ab11b20cc6}

如果 `grout=` 未指定，影像中的灌漿未修改。 如果 `grout= *`顏色`*` 已指定， `*`寬度`*` 預設值 `catalog::GroutWidth`。

## 另請參閱 {#section-8d472906a44943f5a8557e98f2fbc71f}

[顏色值](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/r-ir-color-values.md#reference-657f95c0841742d2a55a48bc938303f6)
