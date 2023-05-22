---
title: 辭彙表
description: 光澤地圖影像。 提供對可重複紋理、牆紙/邊框或貼花的光澤度的逐像素控制。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 922fc527-be19-4d7a-b265-7bdb1de80990
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 2%

---

# 辭彙表 {#glossmap}

光澤地圖影像。 提供對可重複紋理、牆紙/邊框或貼花的光澤度的逐像素控制。

`glossmap={ *`光澤地圖檔案`*| *`嵌入式請求`*}`

<table id="simpletable_6AFC3DEB61D647339525C7CFFA052608"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 嵌入式請求</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph">&amp;lbrace；是&amp;lbrace;'<span class="varname"> 為請求</span>'&amp;rbrace;'&amp;rbrace;|&amp;lbrace;'&amp;lbrace;''<span class="varname"> 外協</span>'&amp;rbrase; </span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 光澤地圖檔案</span> </span> </p></td> 
  <td class="stentry"> <p>光澤圖影像檔案（灰度）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 為請求</span> </span> </p></td> 
  <td class="stentry"> <p>請求到映像伺服器。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 外協 </span> </span> </p></td> 
  <td class="stentry"> <p>請求到外部伺服器。 </p></td> 
 </tr> 
</table>

適用於金屬塗料效果、模切箔壁紙和邊框以及金屬線織物等材料。

光澤圖影像必須為8位灰度級，並且與使用指定的主影像大小相同 `src=`。 請參閱 [ `gloss=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) 的雙曲餘切值。

## 屬性 {#section-26375672d69849be9b026cc93c3bc558}

物料屬性。 由可重複的紋理、牆紙和邊框以及貼花板支援。 被純色、機櫃和窗口覆蓋材料忽略。 請參閱 [ `gloss=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) 的雙曲餘切值。

## 預設 {#section-d9ac031fb2f94482ac3fe2283d7cb168}

無。

## 另請參閱 {#section-33953fc1be82452da37141f2e541e00c}

[光澤=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)。 [src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272)
