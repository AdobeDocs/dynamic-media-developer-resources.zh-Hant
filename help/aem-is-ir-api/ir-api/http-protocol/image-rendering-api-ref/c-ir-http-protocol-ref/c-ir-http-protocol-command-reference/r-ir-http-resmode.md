---
description: 重新取樣模式。 選擇要用於將渲染的影像縮放到使用wid=、hei=或scl=指定的大小的重採樣和/或插值算法。
solution: Experience Manager
title: resMode
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0926dcfe-881c-4b52-b08d-c56afa0ba04d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 8%

---

# resMode{#resmode}

重新取樣模式。 選擇要用於將渲染的影像縮放到使用wid=、hei=或scl=指定的大小的重採樣和/或插值算法。

` `resMode=bilin|bicub|sharp2|bisharp&quot;

<table id="table_AF954C101B30473FAFE9930C7B694305"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> 比林  </span> </p> </td> 
   <td colname="col2"> <p>選擇標準雙線性插值。 最快速的重新取樣方法；可能會有某些明顯的鋸齒狀不自然感。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> bicub  </span> </p> </td> 
   <td colname="col2"> <p>選擇雙立方插值。 與雙線性插值相比，CPU佔用量更大，但會產生更清晰的影像，並產生較少明顯的混疊偽影。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> sharp2  </span> </p> </td> 
   <td colname="col2"> <p>選擇修改的Lanczos窗口函式作為插值算法。 在CPU成本較高的情況下，可能產生比雙bic更尖銳的結果。 </p> <p> <span class="codeph"> sharp已 </span> 由sharp2取 <span class="codeph"> 代， </span>其造成鋸齒偽影（也稱為Moiré）的可能性較小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 比沙爾  </span> </p> </td> 
   <td colname="col2"> <p>選擇<span class="keyword"> Adobe Photoshop </span>預設重採樣器，以減小<span class="keyword"> Adobe Photoshop </span>中稱為「bicubic shear」的影像大小。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-ea7029f37e094d9cb85646b85fbac0ce}

可能發生在要求內的任何位置。 如果未應用最終影像縮放，則忽略。

## 預設 {#section-900872fb93dc41efb3e8ad5b62aadc38}

`attribute::ResMode`

## 另請參閱 {#section-16c557a2250e4f04b3e6cbef18add9ce}

[attribute::ResMode](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cat-resmode.md#reference-fdca7eb6d5104fdeae9d6ac42251db82) ,  [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec),  [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478),  [scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29)
