---
description: 影像錨點（熱點）。 指定可重複紋理或貼花材料的紋理錨點（熱點）。
seo-description: 影像錨點（熱點）。 指定可重複紋理或貼花材料的紋理錨點（熱點）。
seo-title: 錨記
solution: Experience Manager
title: 錨記
topic: Scene7 Image Serving - Image Rendering API
uuid: 1e695882-f97a-4208-b595-2851b91bdbfe
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 錨記{#anchor}

影像錨點（熱點）。 指定可重複紋理或貼花材料的紋理錨點（熱點）。

`anchor= *`xy`*, *``*`

`anchorN= *``*, *`xnyn`*`

<table id="simpletable_1D8E91D8424A424787C4D20C9B040115"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> x</span>, <span class="varname"> y</span> </p></td> 
  <td class="stentry"> <p>源影像左上角的像素偏移(int, int)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> xn</span>, <span class="varname"> yn</span> </p></td> 
  <td class="stentry"> <p>與源影像中心的歸一化偏移（實數、實數）。 </p></td> 
 </tr> 
</table>

可重複的紋理會套用至暈映物件，使紋理錨點( `anchor=`)位於物件的紋理原點。

貼花影像被應用到暈映對象，使得貼花錨點位於對象的貼花原點。 該傾斜位置可以使用該命令進一步 `pos=` 調整。

`anchorN=0,0` 將影像錨點置於來源影像的中央。 `anchorN=-0.5,-0.5` 或 `anchor=0,0` 者位於左上角， `anchorN=0.5,0.5` 位於來源影像的右下角。

## 屬性 {#section-91f929d35cd745ab9e1eeecf45fcedae}

**材料屬性**。 如果或 `align=2`者材料不是可重複的紋理、壁紙或貼紙，則忽略。

## 預設 {#section-b06d728c2f664c29bacf810eefcbde69}

`catalog::Anchor`，則該材料基於目錄條目。 否則， `anchor=0,0` （影像的左上角）是可重複的紋理和桌布， `anchorN=0,0` （影像的中心）是貼文。

## 另請參閱 {#section-b18bf0b035644ca5aedebbc64373718e}

[目錄：：錨點](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-anchor.md#reference-d9b1d49db1fc440686f64b84453297ab) , [align=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-align.md#reference-4d63baa522ce42f9b15167ba34c5c6a7)
