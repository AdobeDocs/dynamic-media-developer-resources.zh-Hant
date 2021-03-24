---
description: 重新取樣模式。 選取重新取樣和／或內插演算法，以將轉換後的影像縮放為使用wid=、hei=或scl=指定的大小。
solution: Experience Manager
title: resMode
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 8%

---


# resMode{#resmode}

重新取樣模式。 選取重新取樣和／或內插演算法，以將轉換後的影像縮放為使用wid=、hei=或scl=指定的大小。

` `resMode=bilin|bicub|sharp2|bisharp&quot;

<table id="table_AF954C101B30473FAFE9930C7B694305"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> bilin  </span> </p> </td> 
   <td colname="col2"> <p>選擇標準雙線性插值。 最快速的重新取樣方法；可能會有某些明顯的鋸齒狀不自然感。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> bicub  </span> </p> </td> 
   <td colname="col2"> <p>選擇雙立方插值。 比雙線性插值耗用的CPU資源更多，但會產生更銳利的影像，並產生較少明顯的鋸齒偽影。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> sharp2  </span> </p> </td> 
   <td colname="col2"> <p>選擇修改的Lanczos窗口函式作為插值算法。 在CPU成本較高的情況下，可能產生比雙立方體更銳利的結果。 </p> <p> <span class="codeph"> sharp </span> 已由sharp2取代， <span class="codeph">  </span>其造成鋸齒偽影（也稱為Moiré）的可能性較小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 比沙爾普  </span> </p> </td> 
   <td colname="col2"> <p>選擇<span class="keyword">Adobe Photoshop</span>預設重新取樣器，以減少<span class="keyword">Adobe Photoshop</span>中稱為"bicubic shear"的影像大小。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-ea7029f37e094d9cb85646b85fbac0ce}

可能發生在請求內的任何位置。 如果未套用最終影像縮放，則忽略。

## 預設 {#section-900872fb93dc41efb3e8ad5b62aadc38}

`attribute::ResMode`

## 另請參閱 {#section-16c557a2250e4f04b3e6cbef18add9ce}

[attribute::ResMode](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cat-resmode.md#reference-fdca7eb6d5104fdeae9d6ac42251db82) ,  [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec),  [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478),  [scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29)
