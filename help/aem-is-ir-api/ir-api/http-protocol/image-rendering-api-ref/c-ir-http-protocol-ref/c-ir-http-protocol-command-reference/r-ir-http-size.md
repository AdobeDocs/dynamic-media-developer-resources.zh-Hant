---
description: 戴卡尺寸。 指定傾斜材料的大小。
solution: Experience Manager
title: 大小
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 3%

---


# 大小{#size}

戴卡尺寸。 指定傾斜材料的大小。

` size= *`寬度，高度`*[ *`，粗細`*]`

<table id="simpletable_00B1226F3B8B49D895D1269AB03D5043"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 寬度、高度  </span> </p> </td> 
  <td class="stentry"> <p>以場景坐標單位（通常為英吋）（實數、實數）表示的貼花物件大小。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 厚度  </span> </p> </td> 
  <td class="stentry"> <p>以場景坐標單位（通常為英吋）（實數）表示的傾斜對象厚度。 </p> </td> 
 </tr> 
</table>

如果寬度和高度都不是0，則影像會縮放至精確指定的尺寸，而影像的外觀比例不會保留。 將任一值設為0會保留影像的寬高比。

如果指定&#x200B;*`thickness`*，則如果暈映物件定義適當的光向量，則會產生下垂式陰影。 將&#x200B;*`thickness`*&#x200B;設為0可停用下垂式陰影演算。

## 屬性 {#section-818e01e91fed4015951189c818ef28d8}

材料屬性。 僅供貼紙使用；被其他材料所忽略。 `res=` 寬度或高度大於0時會忽略。值不得為負數。

## 預設 {#section-f91f516c6af54f0eb4d8c964b923cae0}

`catalog::Size` 以目錄為依據的貼牌材料；否 `size=0,0,0`則。如果未指定&#x200B;*`wid`*&#x200B;和&#x200B;*`hei`*，則從`res=`計算貼文大小。 如果未指定&#x200B;*`thickness`*&#x200B;或將設為0，則不會呈現下垂式陰影。

## 範例 {#section-04fdc2b60b9e4071b672bf6a913738ad}

一種貼花的MSS，其尺寸是根據解析度而定，順時針旋轉20度，厚度為2.5英吋，以獲得適當的下垂式陰影效果：

`…&decal&src=myDecal.png&res=34&rotate=20&size=0,0,2.5&…`

## 另請參閱 {#section-1b116ecd60214732a1757ee1f0cf21c2}

[場景座標](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-scene-coordinates.md#concept-528507024fa640b19a2631357febf7f1), [res=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04)，屬 [性：:Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
