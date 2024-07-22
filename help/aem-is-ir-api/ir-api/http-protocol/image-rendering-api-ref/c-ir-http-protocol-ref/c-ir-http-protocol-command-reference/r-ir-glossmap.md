---
title: glossmap
description: 光澤地圖影像。 提供可重複紋理、壁紙/邊框或貼花的光澤度的逐畫素控制。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 922fc527-be19-4d7a-b265-7bdb1de80990
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 2%

---

# glossmap {#glossmap}

光澤地圖影像。 提供可重複紋理、壁紙/邊框或貼花的光澤度的逐畫素控制。

`glossmap={ *`glossMapFile`*| *`embeddedReq`*}`

<table id="simpletable_6AFC3DEB61D647339525C7CFFA052608"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> embeddedReq</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph">&amp;amp；花括弧；'is&amp;amp；花括弧；'<span class="varname"> isReq</span>'&amp;amp；花括弧；'&amp;amp；花括弧；|&amp;amp；花括弧；'&amp;amp；花括弧；'<span class="varname"> foreignReq</span>'&amp;amp；花括弧；' </span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> glossMapFile</span> </span> </p></td> 
  <td class="stentry"> <p>光澤地圖影像檔案（灰階）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> isReq</span> </span> </p></td> 
  <td class="stentry"> <p>影像伺服器的要求。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> foreignReq </span> </span> </p></td> 
  <td class="stentry"> <p>對外來伺服器的要求。 </p></td> 
 </tr> 
</table>

適用於金屬油漆效果、壓鑄箔牆紙與框線，以及金屬線織物等材料。

光澤地圖影像必須是8位元灰階，而且大小與使用`src=`指定的主要影像相同。 如需其他資訊，請參閱[`gloss=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)的說明。

## 屬性 {#section-26375672d69849be9b026cc93c3bc558}

材質屬性。 支援可重複的紋理、壁紙、框線及貼花。 已被純色、機櫃和視窗覆蓋材料忽略。 如需其他資訊，請參閱[`gloss=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)。

## 預設 {#section-d9ac031fb2f94482ac3fe2283d7cb168}

無。

## 另請參閱 {#section-33953fc1be82452da37141f2e541e00c}

[光澤=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)，[src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272)
