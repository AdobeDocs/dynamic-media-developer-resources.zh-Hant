---
title: 裁切
description: 裁切影像。 指定矩形裁切區域，以畫素表示，或相對於完整解析度來源影像或遮色片影像進行標準化。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d1ea63c1-95f0-4a4e-b65d-eb535eef0205
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 1%

---

# 裁切{#crop}

裁切影像。 指定矩形裁切區域，以畫素表示，或相對於完整解析度來源影像或遮色片影像進行標準化。

`crop= *`座標`*, *`大小`*`

`cropN= *`coordN`*, *`sizeN`*`

<table id="simpletable_472A9AD67AA64419B0877B0535F8B14A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname">順序</span></span> </p> </td> 
  <td class="stentry"> <p>從來源影像左上角到裁切矩形(int， int)左上角的畫素位移。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span></span> </p> </td> 
  <td class="stentry"> <p>從來源影像左上角到裁切矩形左上角的標準化位移（真實、真實）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname">大小</span></span> </p></td> 
  <td class="stentry"> <p>裁切矩形的大小，以畫素為單位(int， int)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname">大小N</span></span> </p></td> 
  <td class="stentry"> <p>相對於來源影像大小（實數、實數）的裁切矩形標準化大小。 </p></td> 
 </tr> 
</table>

也可以透過指定負的x、y值和/或大於影像寬度、高度的寬度、高度值來延伸影像超過其邊界。 在這種情況下，擴充區域是完全透明的（除非指定`bgColor=`）。

## 屬性 {#section-632e0405bb9940679b5f8b1c10e0902e}

Source影像/遮色片屬性。 套用至圖層0來源影像（若`layer=comp`）。 與來源影像或遮色片無關的圖層會略過此專案。

## 預設 {#section-41f62d386c664f77952bc22e7286bb88}

整個影像( `cropN=0,0,1,1`)。

## 範例 {#section-2c99b481c0a04321979a3b522aa295d1}

**裁切左側的10%與右側的10%：**

`…&cropN=0.1,0,0.8,1&…`

**裁切影像底部邊緣20%：**

`…&cropN=0,0,1,0.8&…`

## 另請參閱 {#section-d5616c7aa0ce4faa88f51dd5662e5daf}

[cropPath](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-croppath.md) [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab) ， [錨點=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)， [延伸=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
