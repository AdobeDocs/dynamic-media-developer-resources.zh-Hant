---
title: 群組
description: 圖磚灌漿顏色和粗細。 模擬陶瓷和天然石材磚的灌漿。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6647b459-11d2-47e4-9033-3a740f01a623
TQID: 'https://experienceleague.adobe.com/FrYxcizVu3nXej1tt4QpX0AsLEylXTfwYRaSQP43HNI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 169
ht-degree: 1%

---

# 群組 {#grout}

圖磚灌漿顏色和粗細。 模擬陶瓷和天然石材磚的灌漿。

群組= *`color`*[，*`width`*]

<table id="simpletable_302B78CFC8F14E0F962D1D2064AD1371"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">色彩</span> </span> </p> </td>
  <td class="stentry"> <p>群組顏色（灰色或RGB）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">寬度</span> </span> </p> </td>
  <td class="stentry"> <p>灌漿厚度；場景座標單位（通常為英吋） （實數）。 </p> </td>
 </tr> 
</table>

若要最大程度地控制群組外觀，請套用下列需求：

* 圖磚必須是方形或矩形；目前不支援其他形狀。
* 影像必須僅包含單一圖磚。
* 影像中的預設群組（如果有的話）在所有四個邊緣上必須有相同的厚度。
* 必須在材質目錄( `catalog::GroutWidth`)中指定預設灌漿的厚度。

## 屬性 {#section-de78b678245b4ffda48097c345949e77}

材質屬性。 `*`color`*`必須是RGB色彩值。 `*`width`*`必須是大於或等於0的實數值。

如果重複= 4、5、7、8、9、14或更高，或為可重複紋理以外的材料指定時，則忽略。

## 預設 {#section-bfab3621f70b4489a21994ab11b20cc6}

如果未指定`grout=`，則不會修改影像中的群組。 若指定`grout= *`色彩`*`，`*`寬度`*`預設為`catalog::GroutWidth`。

## 另請參閱 {#section-8d472906a44943f5a8557e98f2fbc71f}

[色彩值](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/r-ir-color-values.md#reference-657f95c0841742d2a55a48bc938303f6)
