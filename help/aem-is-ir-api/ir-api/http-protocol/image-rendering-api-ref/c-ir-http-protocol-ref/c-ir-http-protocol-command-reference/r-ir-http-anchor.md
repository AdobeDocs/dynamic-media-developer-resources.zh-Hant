---
description: 影像錨點（熱點）。 指定可重複紋理或傾倒材料的紋理錨點（熱點）。
solution: Experience Manager
title: 錨記
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ea2c5dce-6eb1-4f05-80bd-7336deb08b9e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 2%

---

# 錨記{#anchor}

影像錨點（熱點）。 指定可重複紋理或傾倒材料的紋理錨點（熱點）。

`anchor= *``*, *`xy`*`

`anchorN= *``*, *`xnyn`*`

<table id="simpletable_1D8E91D8424A424787C4D20C9B040115"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> x</span>,  <span class="varname"> y</span> </p></td> 
  <td class="stentry"> <p>源影像左上角的像素偏移(int、int)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> xn</span>,  <span class="varname"> yn</span> </p></td> 
  <td class="stentry"> <p>從源影像的中心（實、實）歸一化偏移。 </p></td> 
 </tr> 
</table>

可重複的紋理被應用到暈映對象，以便紋理錨點(`anchor=`)位於對象的紋理原點。

將傾斜影像應用於暈映對象，以便傾斜錨點位於對象的傾斜原點。 可使用`pos=`命令進一步調整傾斜位置。

`anchorN=0,0` 將影像錨點置於源影像的中心。`anchorN=-0.5,-0.5` 或 `anchor=0,0` 者位於左上角， `anchorN=0.5,0.5` 而位於源影像的右下角。

## 屬性 {#section-91f929d35cd745ab9e1eeecf45fcedae}

**材料屬性**。如果`align=2`，或材料不是可重複的紋理、壁紙或傾斜，則忽略。

## 預設 {#section-b06d728c2f664c29bacf810eefcbde69}

`catalog::Anchor`，如果資料是以目錄項目為基礎。否則，`anchor=0,0`（影像的左上角）是可重複的紋理和壁紙，`anchorN=0,0`（影像的中心）是十個。

## 另請參閱 {#section-b18bf0b035644ca5aedebbc64373718e}

[目錄：：錨點](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-anchor.md#reference-d9b1d49db1fc440686f64b84453297ab) ,  [align=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-align.md#reference-4d63baa522ce42f9b15167ba34c5c6a7)
