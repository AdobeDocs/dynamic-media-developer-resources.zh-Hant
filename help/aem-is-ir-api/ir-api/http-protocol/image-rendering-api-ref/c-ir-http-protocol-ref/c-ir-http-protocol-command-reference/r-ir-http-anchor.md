---
title: 錨記
description: 影像錨點（熱點）。 指定可重複紋理或貼花材料的紋理錨點（熱點）。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ea2c5dce-6eb1-4f05-80bd-7336deb08b9e
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 3%

---

# 錨記{#anchor}

影像錨點（熱點）。 指定可重複紋理或貼花材料的紋理錨點（熱點）。

`anchor= *`x`*, *`y`*`

`anchorN= *`x`*, *`英`*`

<table id="simpletable_1D8E91D8424A424787C4D20C9B040115"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> x</span>。 <span class="varname"> y</span> </p></td> 
  <td class="stentry"> <p>源影像左上角的像素偏移(int, int)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> x</span>。 <span class="varname"> 英</span> </p></td> 
  <td class="stentry"> <p>從源影像中心歸一化的偏移（實數、實數）。 </p></td> 
 </tr> 
</table>

可重複的紋理被應用於視頻對象，以便紋理錨點( `anchor=`)位於對象的紋理原點。

貼花影像被應用於貼花對象，使得貼花錨點位於對象貼花原點處。 該傾斜位置可進一步使用 `pos=` 的子菜單。

`anchorN=0,0` 將影像錨點置於源影像的中心。 `anchorN=-0.5,-0.5` 或 `anchor=0,0` 在左上角 `anchorN=0.5,0.5` 位於源影像的右下角。

## 屬性 {#section-91f929d35cd745ab9e1eeecf45fcedae}

**物料屬性**。 如果忽略 `align=2`或者，如果材料不是可重複的紋理、壁紙或貼花。

## 預設 {#section-b06d728c2f664c29bacf810eefcbde69}

`catalog::Anchor`，如果物料基於目錄條目。 否則， `anchor=0,0` （影像左上角）可重複紋理和壁紙， `anchorN=0,0` （影像中心）。

## 另請參閱 {#section-b18bf0b035644ca5aedebbc64373718e}

[目錄：：錨點](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-anchor.md#reference-d9b1d49db1fc440686f64b84453297ab) 。 [對齊=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-align.md#reference-4d63baa522ce42f9b15167ba34c5c6a7)
