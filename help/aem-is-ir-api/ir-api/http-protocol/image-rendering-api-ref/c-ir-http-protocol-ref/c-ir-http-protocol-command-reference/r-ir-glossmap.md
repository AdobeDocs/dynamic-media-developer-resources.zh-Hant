---
description: 光澤地圖影像。 提供逐個像素的可重複紋理、壁紙／邊框或貼紙的光澤度控制。
solution: Experience Manager
title: glosmap
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 3%

---


# glossmap{#glossmap}

光澤地圖影像。 提供逐個像素的可重複紋理、壁紙／邊框或貼紙的光澤度控制。

`glossmap={ *`GlossMapFileembeddedReq`*| *``*}`

<table id="simpletable_6AFC3DEB61D647339525C7CFFA052608"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> embeddedReq</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph">&amp;lbrace;'is&amp;<span class="varname"> lbrace;'isReq</span>'&amp;rbrace;'&amp;rbrace;|&amp;lbrace;'&amp;lbrace;''<span class="varname"> foreignReq</span>'&amp;rbrace;'  </span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> glossMapFile</span> </span> </p></td> 
  <td class="stentry"> <p>光澤地圖影像檔（灰階）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> isReq</span> </span> </p></td> 
  <td class="stentry"> <p>向影像伺服器要求。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> foreignReq  </span> </span> </p></td> 
  <td class="stentry"> <p>向外部伺服器請求。 </p></td> 
 </tr> 
</table>

適用於金屬漆效果、模切箔壁紙和邊框、金屬線織物等材料。

光澤地圖影像必須是8位元灰階，而且大小必須與使用`src=`指定的主要影像完全相同。 如需詳細資訊，請參閱[ `gloss=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)的說明。

## 屬性 {#section-26375672d69849be9b026cc93c3bc558}

材料屬性。 由可重複的紋理、桌布和邊框以及貼文支援。 被純色、機櫃和窗口覆蓋材料忽略。 如需詳細資訊，請參閱[ `gloss=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)。

## 預設 {#section-d9ac031fb2f94482ac3fe2283d7cb168}

無。

## 另請參閱 {#section-33953fc1be82452da37141f2e541e00c}

[光澤=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca), [src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272)
