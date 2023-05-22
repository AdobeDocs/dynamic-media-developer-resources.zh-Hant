---
title: BGC
description: 背景顏色. 指定可著色紋理和貼花的減色顏色。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9ac6517e-b9c3-48d9-97ac-d8aa65a8ba46
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 5%

---

# BGC {#bgc}

背景顏色. 指定可著色紋理和貼花的減色顏色。

`bgc= *[!DNL color]*`

<table id="simpletable_131302355CAB4900A7B45FED903A1AAD" class="- topic/simpletable "> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p><span class="+ topic/keyword sw-d/varname varname"> color</span> </p> </td> 
  <td class="- topic/stentry stentry"> <p>RGB或灰色值。 </p></td> 
 </tr> 
</table>

影像渲染的紋理著色算法簡單明瞭，即影像的分量值 `bgc=` 從紋理像素值中減去； `color=` 添加，最後將結果剪切到 `0,0,0` 和 `255,255,255`。

對於紋理著色的典型用途， `bgc=` 可能是紋理影像中最重要的顏色或主色。 Dynamic Media影像創作提供了半自動工具，可提取合理的 `bgc=` 紋理影像中的顏色值。

當紋理材料被施加到非紋理可變的紋理對象時， `bgc=` 將作為前景色應用 `color=` 未指定。

## 屬性 {#section-b2db6f147d7f443ba9f671de04c2ef19}

物料屬性。 被純色和機櫃材料忽略。

## 預設 {#section-de10ef5985ee4ae1ba56d14ba8512b81}

`catalog::BaseColor` 如果物料基於目錄條目，否則 `bgc=808080` （中性灰色）。

## 範例 {#section-bf5f0f296bc448ed9d5a84afabcf81e6}

對織構具有主要RGB色120,34,193的服裝織物進行著色：

`…&src=fabrics/d213.jpg&res=40&bgc=120,34,193&color=140,95,100&…`

## 另請參閱 {#section-de9958dd63a742b4b5d780c59a57da33}

[目錄：:BaseColor](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-basecolor.md#reference-5f02371b1d8e444ab12d2614d9792de8) 。 [顏色=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa)
