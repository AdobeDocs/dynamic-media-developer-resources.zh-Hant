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
ht-degree: 2%

---

# 錨記{#anchor}

影像錨點（熱點）。 指定可重複紋理或貼花材料的紋理錨點（熱點）。

`anchor= *`x`*, *`y`*`

`anchorN= *`xn`*, *`yn`*`

<table id="simpletable_1D8E91D8424A424787C4D20C9B040115"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> x</span>，<span class="varname"> y</span> </p></td> 
  <td class="stentry"> <p>從來源影像左上角的畫素位移(int， int)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> xn</span>，<span class="varname"> yn</span> </p></td> 
  <td class="stentry"> <p>從來源影像中心的標準化位移（實數、實數）。 </p></td> 
 </tr> 
</table>

重複紋理會套用至暈映物件，使紋理錨點(`anchor=`)位於物件的紋理原點。

貼花影像會套用至暈映物件，使貼花錨點位於物件的貼花原點。 可以使用`pos=`命令進一步調整貼花位置。

`anchorN=0,0`將影像錨點放在來源影像的中央。 `anchorN=-0.5,-0.5`或`anchor=0,0`位於左上角，`anchorN=0.5,0.5`位於來源影像的右下角。

## 屬性 {#section-91f929d35cd745ab9e1eeecf45fcedae}

**材質屬性**。 若`align=2`，或材質不是可重複的材質、壁紙或貼花，則忽略此項。

## 預設 {#section-b06d728c2f664c29bacf810eefcbde69}

`catalog::Anchor` （如果素材是以目錄專案為基礎）。 否則，`anchor=0,0` （影像左上角）代表可重複的紋理和壁紙，而`anchorN=0,0` （影像中心）代表貼花。

## 另請參閱 {#section-b18bf0b035644ca5aedebbc64373718e}

[目錄：：錨點](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-anchor.md#reference-d9b1d49db1fc440686f64b84453297ab) ， [對齊=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-align.md#reference-4d63baa522ce42f9b15167ba34c5c6a7)
