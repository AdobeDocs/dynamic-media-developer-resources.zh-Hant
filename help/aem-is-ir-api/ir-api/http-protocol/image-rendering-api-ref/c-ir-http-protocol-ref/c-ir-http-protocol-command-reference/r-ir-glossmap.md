---
description: 光澤地圖影像。 提供逐個像素的可重複紋理、壁紙／邊框或貼紙的光澤度控制。
seo-description: 光澤地圖影像。 提供逐個像素的可重複紋理、壁紙／邊框或貼紙的光澤度控制。
seo-title: glosmap
solution: Experience Manager
title: glosmap
topic: Scene7 Image Serving - Image Rendering API
uuid: f137d362-74a1-45b3-9274-a3a2d6cf5db0
translation-type: tm+mt
source-git-commit: 515fcf8488eba7d9ca501a4182eaa73f1936488b
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 2%

---


# glosmap{#glossmap}

光澤地圖影像。 提供逐個像素的可重複紋理、壁紙／邊框或貼紙的光澤度控制。

`glossmap={ *`GlossMapFileembeddedReq`*| *``*}`

<table id="simpletable_6AFC3DEB61D647339525C7CFFA052608"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> embeddedReq</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph">&amp;lbrace;'is&amp;lbrace;'<span class="varname"> isReq</span>'&amp;rbrace;'&amp;rbrace;|&amp;'&amp;lbrace;'<span class="varname"> foreinReq</span>'&amp;rbrace;' </span> </p></td> 
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
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> foreignReq </span> </span> </p></td> 
  <td class="stentry"> <p>向外部伺服器請求。 </p></td> 
 </tr> 
</table>

適用於金屬漆效果、模切箔壁紙和邊框、金屬線織物等材料。

光澤地圖影像必須是8位元灰階，而且大小必須與使用指定的主要影像完全相同 `src=`。 如需詳細資訊，請 [ 參閱 `gloss=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) 的說明。

## 屬性 {#section-26375672d69849be9b026cc93c3bc558}

材料屬性。 由可重複的紋理、桌布和邊框以及貼文支援。 被純色、機櫃和窗口覆蓋材料忽略。 See [ `gloss=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) for additional information.

## 預設 {#section-d9ac031fb2f94482ac3fe2283d7cb168}

無。

## 另請參閱 {#section-33953fc1be82452da37141f2e541e00c}

[光澤=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca), [src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272)
