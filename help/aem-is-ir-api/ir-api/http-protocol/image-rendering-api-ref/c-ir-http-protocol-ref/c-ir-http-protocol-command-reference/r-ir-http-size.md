---
description: 傾斜大小。 指定傾斜材料的大小。
solution: Experience Manager
title: 大小
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 756d8b9f-076a-48d6-95c9-e0d6caeed3dd
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 3%

---

# 大小{#size}

傾斜大小。 指定傾斜材料的大小。

` size= *`寬度，高度`*[ *`，粗細`*]`

<table id="simpletable_00B1226F3B8B49D895D1269AB03D5043"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 寬度、高度  </span> </p> </td> 
  <td class="stentry"> <p>以場景坐標單位表示的十字對象的大小（通常為英吋）（實數、實數）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 粗細  </span> </p> </td> 
  <td class="stentry"> <p>以場景坐標單位（通常為英吋）（實數）表示的十字對象的厚度。 </p> </td> 
 </tr> 
</table>

如果寬度和高度都不是0，則影像會縮放到精確指定的尺寸，並且不會保留影像的長寬比。 將任一值設定為0可保留影像的外觀比例。

如果指定&#x200B;*`thickness`*，則如果暈映對象定義了適當的光向量，則會呈現陰影。 將&#x200B;*`thickness`*&#x200B;設定為0以禁用陰影呈現。

## 屬性 {#section-818e01e91fed4015951189c818ef28d8}

材料屬性。 僅用於十字；被其他材料忽略。 `res=` 如果寬度或高度大於0，則會忽略。值不得為負數。

## 預設 {#section-f91f516c6af54f0eb4d8c964b923cae0}

`catalog::Size` （二）以目錄條目為依據的；否則 `size=0,0,0`。如果未指定&#x200B;*`wid`*&#x200B;和&#x200B;*`hei`*，或將設為0，則從`res=`計算該小數。 如果未指定&#x200B;*`thickness`*&#x200B;或將設定為0，則不呈現投影。

## 範例 {#section-04fdc2b60b9e4071b672bf6a913738ad}

用於十字的MSS，其尺寸基於解析度，順時針旋轉20度，厚度為2.5英吋，以獲得適當的陰影效果：

`…&decal&src=myDecal.png&res=34&rotate=20&size=0,0,2.5&…`

## 另請參閱 {#section-1b116ecd60214732a1757ee1f0cf21c2}

[場景座標](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-scene-coordinates.md#concept-528507024fa640b19a2631357febf7f1),  [res=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04)，屬 [性：:Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
