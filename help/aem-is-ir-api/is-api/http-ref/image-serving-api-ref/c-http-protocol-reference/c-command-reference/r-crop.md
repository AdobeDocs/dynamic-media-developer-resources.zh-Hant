---
description: 裁切影像。 指定矩形裁切區域，以像素表示，或相對於全解析度源影像或遮色片影像標準化。
seo-description: 裁切影像。 指定矩形裁切區域，以像素表示，或相對於全解析度源影像或遮色片影像標準化。
seo-title: 裁切
solution: Experience Manager
title: 裁切
topic: Scene7 Image Serving - Image Rendering API
uuid: c8eca467-7564-48a6-82d7-17f68a1399e1
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f

---


# 裁切{#crop}

裁切影像。 指定矩形裁切區域，以像素表示，或相對於全解析度源影像或遮色片影像標準化。

`crop= *`坐`*, *`標`*`

`cropN= *``*, *`coordNsizeN`*`

<table id="simpletable_472A9AD67AA64419B0877B0535F8B14A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 坐標</span></span> </p> </td> 
  <td class="stentry"> <p>從來源影像的左上角到裁切矩形的左上角的像素偏移(int, int)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span></span> </p> </td> 
  <td class="stentry"> <p>從來源影像的左上角標準化偏移至裁切直角的左上角（實數、實數）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> 大小 <span class="varname"></span></span> </p></td> 
  <td class="stentry"> <p>裁切的大小以像素為單位(int、int)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> 大 <span class="varname"> 小N</span></span> </p></td> 
  <td class="stentry"> <p>相對於源影像（實數、實數）的大小，裁切的標準化大小正確。 </p></td> 
 </tr> 
</table>

也可以通過指定負x、y值和／或寬度、高度值（大於影像寬度、高度），將影像延伸超出其邊界。 在這種情況下，延伸區域是完全透明的(除非 `bgColor=` 指定)。

## 屬性 {#section-632e0405bb9940679b5f8b1c10e0902e}

來源影像／遮色片屬性。 如果適用，則套用至0層來源影像 `layer=comp`。 被未與源影像或蒙版關聯的圖層忽略。

## 預設 {#section-41f62d386c664f77952bc22e7286bb88}

整個影像( `cropN=0,0,1,1`)。

## 範例 {#section-2c99b481c0a04321979a3b522aa295d1}

**將左邊10%的作物裁切為右邊10%:**

`…&cropN=0.1,0,0.8,1&…`

**裁切影像底部邊緣20%:**

`…&cropN=0,0,1,0.8&…`

## 另請參閱 {#section-d5616c7aa0ce4faa88f51dd5662e5daf}

[cropPath](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-croppath.md) [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab) ，錨 [記=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c), [延伸=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
