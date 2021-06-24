---
description: 路徑文字屬性。
solution: Experience Manager
title: pathAttr
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: fdf9274a-70d0-4692-a7a9-c108abb9ab84
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 3%

---

# pathAttr{#pathattr}

路徑文字屬性。

` pathAttr= *``*[, *``*[, *`directionstartPosendPos`*]]`

<table id="simpletable_EC76095316AF4F07B1DDCC0D72B814CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 方向 </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> 規範  </span> |反 <span class="codeph"> 向  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> startPos  </span> </p> </td> 
  <td class="stentry"> <p>路徑上的文字開始位置（實數0.0...1.0）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> endPos  </span> </p> </td> 
  <td class="stentry"> <p>路徑上的文本結束位置（實數0.0...&lt;2.0）。 </p> </td> 
 </tr> 
</table>

指定`norm`以從第一個路徑頂點附近開始繪製文本，指定`reverse`以從最後一個頂點附近開始沿相反方向繪製文本。

*`startPos`* 並 *`endPos`* 允許調整路徑上將繪製文本的位置。0.0對應於路徑中的第一個頂點，1.0對應於最後一個頂點；中間值表示沿著第一頂點和最後一個頂點之間的路徑的距離。

## 屬性 {#section-80f266da4e2549d89f022a3f9ff4584d}

層屬性。 如果層未包含`textPs=`和`textPath=`命令，則忽略。

*`startPos`* 必須大於或等於0且小於1.0。 *`endPos`* 應用於 *`startPos`* 開放路徑時必須大於或等於1.0，或應用於封閉路徑時必須小於或等於( *`startPos`* + 1.0)。

## 預設 {#section-3e757970885c45e7b6100e78dc08626f}

`pathAttr=norm,0,1`

## 另請參閱 {#section-b869745de1da4ef996dfda4af39ed14d}

[textPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textpath.md#reference-b09cc0902dff4725bdb54d5da4076ccd) ,  [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767)
