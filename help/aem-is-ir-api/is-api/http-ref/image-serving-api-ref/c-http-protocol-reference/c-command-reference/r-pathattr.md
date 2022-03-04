---
description: 路徑上的文本屬性。
solution: Experience Manager
title: 路徑屬性
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fdf9274a-70d0-4692-a7a9-c108abb9ab84
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 3%

---

# 路徑屬性{#pathattr}

路徑上的文本屬性。

` pathAttr= *`方向`*[, *`開始POS`*[, *`結束POS`*]]`

<table id="simpletable_EC76095316AF4F07B1DDCC0D72B814CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 方向 </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> 范數 </span> | <span class="codeph"> 逆 </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 開始POS </span> </p> </td> 
  <td class="stentry"> <p>路徑上的文本起始位置（實數0.0..1.0）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 結束POS </span> </p> </td> 
  <td class="stentry"> <p>路徑上的文本結束位置（實數0.0..&lt;2.0）。 </p> </td> 
 </tr> 
</table>

指定 `norm` 繪製第一個路徑頂點附近的文本， `reverse` 在最後一個頂點附近繪製相反方向的文本。

*`startPos`* 和 *`endPos`* 允許調整繪製文本的路徑上的位置。 0.0對應於路徑中的第一個頂點，1.0對應於最後一個頂點；中間值表示沿第一頂點和最後一個頂點之間的路徑的距離。

## 屬性 {#section-80f266da4e2549d89f022a3f9ff4584d}

層屬性。 如果層不包括，則忽略 `textPs=` 和 `textPath=` 的雙曲餘切值。

*`startPos`* 必須大於或等於0且小於1.0。 *`endPos`* 必須大於 *`startPos`* 當應用於開路徑時小於或等於1.0，或小於或等於( *`startPos`* + 1.0)。

## 預設 {#section-3e757970885c45e7b6100e78dc08626f}

`pathAttr=norm,0,1`

## 另請參閱 {#section-b869745de1da4ef996dfda4af39ed14d}

[textPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textpath.md#reference-b09cc0902dff4725bdb54d5da4076ccd) 。 [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767)
