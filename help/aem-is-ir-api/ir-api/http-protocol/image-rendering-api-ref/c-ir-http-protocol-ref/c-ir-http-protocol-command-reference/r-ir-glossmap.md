---
description: 光澤圖影像。 提供可重複紋理、壁紙/邊框或傾斜的光澤度的逐像素控制。
solution: Experience Manager
title: 辭匯圖
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 922fc527-be19-4d7a-b265-7bdb1de80990
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 3%

---

# 辭匯圖{#glossmap}

光澤圖影像。 提供可重複紋理、壁紙/邊框或傾斜的光澤度的逐像素控制。

`glossmap={ *``*| *`glossMapFileembeddedReq`*}`

<table id="simpletable_6AFC3DEB61D647339525C7CFFA052608"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> embeddedReq</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph">&amp;lbrace;'is&amp;lbrace;'<span class="varname"> isReq</span>'&amp;rbrace;'&amp;rbrace;|&amp;lbrace;'&amp;lbrace;''<span class="varname"> foreignReq</span>'&amp;rbrace;'  </span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> glossMapFile</span> </span> </p></td> 
  <td class="stentry"> <p>光澤圖影像檔案（灰度）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> isReq</span> </span> </p></td> 
  <td class="stentry"> <p>請求影像伺服器。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> foreignReq  </span> </span> </p></td> 
  <td class="stentry"> <p>向外部伺服器發出請求。 </p></td> 
 </tr> 
</table>

適用於金屬塗料效果、模切箔壁紙和邊框、金屬線織物等材料。

光澤圖影像必須是8位灰度，並且大小與使用`src=`指定的主影像完全相同。 如需詳細資訊，請參閱[ `gloss=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)說明。

## 屬性 {#section-26375672d69849be9b026cc93c3bc558}

材料屬性。 由可重複的紋理、壁紙和邊框以及標籤支援。 被固色、機箱和覆蓋材料的窗戶忽略。 如需詳細資訊，請參閱[ `gloss=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) 。

## 預設 {#section-d9ac031fb2f94482ac3fe2283d7cb168}

無。

## 另請參閱 {#section-33953fc1be82452da37141f2e541e00c}

[gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca),  [src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272)
