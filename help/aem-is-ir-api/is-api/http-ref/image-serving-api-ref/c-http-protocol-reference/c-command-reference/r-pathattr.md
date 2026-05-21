---
title: pathAttr
description: 路徑文字屬性。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fdf9274a-70d0-4692-a7a9-c108abb9ab84
TQID: 'https://experienceleague.adobe.com/A7uOgsYtOH6AmVOtbUfQDVJHwJEkCSXqBYavY9CbRkw'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 154
ht-degree: 1%

---

# pathAttr{#pathattr}

路徑文字屬性。

` pathAttr= *`方向`*[, *`startPos`*[, *`endPos`*]]`

<table id="simpletable_EC76095316AF4F07B1DDCC0D72B814CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname">方向</span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph">標準</span> | <span class="codeph">反向</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> startPos </span> </p> </td> 
  <td class="stentry"> <p>路徑上的文字起始位置（實數0.0...1.0）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> endPos </span> </p> </td> 
  <td class="stentry"> <p>路徑上的文字結束位置（實數0.0...&lt;2.0）。 </p> </td> 
 </tr> 
</table>

指定`norm`繪製從第一個路徑頂點附近的文字，指定`reverse`以相反方向繪製文字，從最後一個頂點附近開始。

*`startPos`*&#x200B;和&#x200B;*`endPos`*&#x200B;允許調整文字繪製路徑上的位置。 0.0對應於路徑中的第一個頂點，1.0對應於最後一個頂點；中間值表示沿著路徑第一個和最後一個頂點之間的距離。

## 屬性 {#section-80f266da4e2549d89f022a3f9ff4584d}

圖層屬性。 如果圖層不包含`textPs=`和`textPath=`命令，則忽略。

*`startPos`*&#x200B;必須大於或等於0且小於1.0。 *`endPos`*&#x200B;在套用至開放路徑時必須大於&#x200B;*`startPos`*&#x200B;且小於或等於1.0，或在套用至封閉路徑時小於或等於( *`startPos`* + 1.0)。

## 預設 {#section-3e757970885c45e7b6100e78dc08626f}

`pathAttr=norm,0,1`

## 另請參閱 {#section-b869745de1da4ef996dfda4af39ed14d}

[textPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textpath.md#reference-b09cc0902dff4725bdb54d5da4076ccd) ， [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767)
