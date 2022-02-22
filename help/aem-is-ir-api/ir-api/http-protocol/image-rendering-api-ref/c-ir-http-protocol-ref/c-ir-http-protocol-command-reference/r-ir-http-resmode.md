---
title: resMode
description: 重新取樣模式。 選擇重新採樣和/或插值算法，以將渲染的影像縮放到使用wid=、hei=或scl=指定的大小。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0926dcfe-881c-4b52-b08d-c56afa0ba04d
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 8%

---

# resMode{#resmode}

重新取樣模式。 選擇重採樣和/或插值算法，用於將渲染的影像縮放到指定的大小 `wid=`。 `hei=`或 `scl=`。

` `resMode=bilin|bicub|sharp2|bisharp&quot;

<table id="table_AF954C101B30473FAFE9930C7B694305"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> 比林 </span> </p> </td> 
   <td colname="col2"> <p>選擇標準雙線性插值。 最快速的重新取樣方法；可能會有某些明顯的鋸齒狀不自然感。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> 比克 </span> </p> </td> 
   <td colname="col2"> <p>選擇雙三次插值。 與雙線性插值相比，CPU佔用更多，但生成的影像更清晰，鋸齒偽影較少。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> 銳2 </span> </p> </td> 
   <td colname="col2"> <p>選擇修改的Lanczos窗函式作為插值算法。 在CPU成本較高的情況下，結果可能比雙三次方的結果更為明顯。 </p> <p> <span class="codeph"> 鋒利 </span> 已替換為 <span class="codeph"> 銳2 </span>，其導致鋸齒偽影的可能性較小，也稱為Moiré。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 比沙爾 </span> </p> </td> 
   <td colname="col2"> <p>選擇 <span class="keyword"> Adobe Photoshop </span> 用於減小影像大小的預設重採樣器，在中稱為「雙三次銳化」 <span class="keyword"> Adobe Photoshop </span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-ea7029f37e094d9cb85646b85fbac0ce}

請求中的任何位置都可能發生。 如果未應用最終影像縮放，則忽略。

## 預設 {#section-900872fb93dc41efb3e8ad5b62aadc38}

`attribute::ResMode`

## 另請參閱 {#section-16c557a2250e4f04b3e6cbef18add9ce}

[屬性：:ResMode](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cat-resmode.md#reference-fdca7eb6d5104fdeae9d6ac42251db82) 。 [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec)。 [黑=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)。 [scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29)
