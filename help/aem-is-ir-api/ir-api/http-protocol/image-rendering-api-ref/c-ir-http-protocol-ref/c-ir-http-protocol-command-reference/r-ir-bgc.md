---
description: 背景顏色. 指定可上色紋理和底色的減色顏色。
solution: Experience Manager
title: bgc
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 6%

---


# bgc{#bgc}

背景顏色. 指定可上色紋理和底色的減色顏色。

`bgc= *[!DNL color]*`

<table id="simpletable_131302355CAB4900A7B45FED903A1AAD" class="- topic/simpletable "> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p><span class="+ topic/keyword sw-d/varname varname"> color</span> </p> </td> 
  <td class="- topic/stentry stentry"> <p>RGB或灰色值。 </p></td> 
 </tr> 
</table>

影像渲染的紋理上色算法非常簡單——從紋理像素中減去`bgc=`的分量值，添加`color=`，最後將結果裁剪到`0,0,0`和`255,255,255`。

對於紋理著色的典型用途，`bgc=`的值可能是紋理影像中最重要或最主要的顏色。 Dynamic Media影像製作提供半自動工具，可從紋理影像擷取合理的`bgc=`色彩值。

當紋理材料應用於非可紋理的暈映對象時，如果未指定`color=`,`bgc=`將作為前景顏色應用。

## 屬性 {#section-b2db6f147d7f443ba9f671de04c2ef19}

材料屬性。 被純色和機櫃材料忽略。

## 預設 {#section-de10ef5985ee4ae1ba56d14ba8512b81}

`catalog::BaseColor` 如果材料基於目錄條目，則 `bgc=808080` 否（中性灰色）。

## 範例 {#section-bf5f0f296bc448ed9d5a84afabcf81e6}

將服裝織物上色，其紋理具有主導RGB顏色120,34,193:

`…&src=fabrics/d213.jpg&res=40&bgc=120,34,193&color=140,95,100&…`

## 另請參閱 {#section-de9958dd63a742b4b5d780c59a57da33}

[catalog:::BaseColor](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-basecolor.md#reference-5f02371b1d8e444ab12d2614d9792de8) ,  [color=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa)
