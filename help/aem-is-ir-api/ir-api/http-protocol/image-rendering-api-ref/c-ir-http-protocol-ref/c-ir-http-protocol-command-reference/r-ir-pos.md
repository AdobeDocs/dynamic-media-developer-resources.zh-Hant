---
title: pos
description: 貼花位置。 定義從貼花影像的anchor=點到目標暈映物件所定義的貼花原點的位移（英吋）。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 531f1465-2bec-46b6-a41e-54d993cbf410
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 3%

---

# pos{#pos}

貼花位置。 定義從貼花影像的anchor=點到目標暈映物件所定義的貼花原點的位移（英吋）。

`pos=x,y`

<table id="simpletable_DB3B64EFB67A47AD843812324ABFAE45"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> x</span>，<span class="varname"> y</span> </p></td> 
  <td class="stentry"> <p>以場景座標單位（通常為英吋） （實數、實數）調整相對位置。 </p></td> 
 </tr> 
</table>

## 屬性 {#section-50371cfa4e244bc49d2295a918749258}

材質屬性。 被貼花以外的材料忽略。

## 預設 {#section-1b66efab054c45ca8d67d6a9865020f4}

`pos=0,0`. 將貼花的錨點對齊暈映物件的貼花原點。

## 另請參閱 {#section-7cd8139481334ed79704d628b5bbd236}

[場景座標](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-scene-coordinates.md#concept-528507024fa640b19a2631357febf7f1)， [anchor=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
