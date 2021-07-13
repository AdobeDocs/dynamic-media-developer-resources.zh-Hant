---
description: 裁切影像。 指定矩形裁切區域，以像素表示，或相對於全解析度源影像或蒙版影像進行標準化。
solution: Experience Manager
title: 裁切
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d1ea63c1-95f0-4a4e-b65d-eb535eef0205
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 3%

---

# 裁切{#crop}

裁切影像。 指定矩形裁切區域，以像素表示，或相對於全解析度源影像或蒙版影像進行標準化。

`crop= *``*, *`coordsize`*`

`cropN= *``*, *`coordNsizeN`*`

<table id="simpletable_472A9AD67AA64419B0877B0535F8B14A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 坐標</span></span> </p> </td> 
  <td class="stentry"> <p>從源影像的左上角到裁切直線的左上角的像素偏移(int、int)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span></span> </p> </td> 
  <td class="stentry"> <p>從源影像的左上角到裁切直接的左上角（實數、實數）歸一化偏移。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 大小</span></span> </p></td> 
  <td class="stentry"> <p>裁切直接的大小（像素，整）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> sizeN</span></span> </p></td> 
  <td class="stentry"> <p>相對於源影像（實、實）的大小，裁切的歸一化大小直接。 </p></td> 
 </tr> 
</table>

還可以通過指定負x、y值和/或寬度、大於影像寬度、高度的高度值來將影像擴展到其邊界之外。 在這種情況下，擴展區域是完全透明的（除非指定`bgColor=`）。

## 屬性 {#section-632e0405bb9940679b5f8b1c10e0902e}

源影像/掩碼屬性。 如果`layer=comp`，則應用於0層源影像。 被未與源影像或掩碼關聯的層忽略。

## 預設 {#section-41f62d386c664f77952bc22e7286bb88}

整個影像(`cropN=0,0,1,1`)。

## 範例 {#section-2c99b481c0a04321979a3b522aa295d1}

**左邊10%，右邊10%:**

`…&cropN=0.1,0,0.8,1&…`

**裁切影像底邊20%:**

`…&cropN=0,0,1,0.8&…`

## 另請參閱 {#section-d5616c7aa0ce4faa88f51dd5662e5daf}

[](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-croppath.md) [cropPathbgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab) ,  [anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c),  [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
