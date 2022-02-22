---
title: 大小
description: 德卡爾大小。 指定貼花材料的大小。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 756d8b9f-076a-48d6-95c9-e0d6caeed3dd
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 3%

---

# 大小{#size}

德卡爾大小。 指定貼花材料的大小。

` size= *`寬度，高度`*[ *`厚度`*]`

<table id="simpletable_00B1226F3B8B49D895D1269AB03D5043"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 寬度，高度 </span> </p> </td> 
  <td class="stentry"> <p>以場景坐標單位（通常為英吋）（實數、實數）表示的貼花對象大小。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 厚度 </span> </p> </td> 
  <td class="stentry"> <p>以場景坐標單位（通常為英吋）（實數）表示的貼花對象的厚度。 </p> </td> 
 </tr> 
</table>

如果寬度或高度均不為0，則影像將縮放到精確指定的尺寸，並且不保留影像的長寬比。 將任一值設定為0可保留影像的長寬比。

如果 *`thickness`* 如果已指定，則當vignette對象定義適當的光向量時，將呈現投影。 設定 *`thickness`* 到0以禁用投影渲染。

## 屬性 {#section-818e01e91fed4015951189c818ef28d8}

物料屬性。 僅用於貼花；被其他材料忽略。 `res=` 寬度或高度大於0時忽略。 值不得為負。

## 預設 {#section-f91f516c6af54f0eb4d8c964b923cae0}

`catalog::Size` 以目錄條目為基礎的貼牌材料；否則 `size=0,0,0`。 傾斜尺寸由 `res=` 如果 *`wid`* 和 *`hei`* 未指定或設定為0。 如果 *`thickness`* 未指定或設定為0。

## 範例 {#section-04fdc2b60b9e4071b672bf6a913738ad}

用於貼花的MSS，其尺寸根據解析度確定，順時針旋轉20°，厚度為2.5英吋，以獲得適當的投影效果：

`…&decal&src=myDecal.png&res=34&rotate=20&size=0,0,2.5&…`

## 另請參閱 {#section-1b116ecd60214732a1757ee1f0cf21c2}

[場景坐標](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-scene-coordinates.md#concept-528507024fa640b19a2631357febf7f1)。 [雷斯=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04)。 [屬性：：解析度](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
