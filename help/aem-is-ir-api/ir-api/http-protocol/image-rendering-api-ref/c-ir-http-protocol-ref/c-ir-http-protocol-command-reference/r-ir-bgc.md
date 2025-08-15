---
title: bgc
description: 背景顏色。 指定可上色紋理和貼花的減色色彩。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9ac6517e-b9c3-48d9-97ac-d8aa65a8ba46
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 2%

---

# bgc {#bgc}

背景顏色。 指定可上色紋理和貼花的減色色彩。

`bgc= *[!DNL color]*`

<table id="simpletable_131302355CAB4900A7B45FED903A1AAD" class="- topic/simpletable "> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p><span class="+ topic/keyword sw-d/varname varname">色彩</span> </p> </td> 
  <td class="- topic/stentry stentry"> <p>RGB或灰色的值。 </p></td> 
 </tr> 
</table>

影像演算的紋理上色演演算法簡單明瞭 — 從紋理畫素值中減去`bgc=`的元件值；新增`color=`，最後將結果剪裁為`0,0,0`和`255,255,255`。

對於紋理上色的一般使用，`bgc=`的值可能是紋理影像中最重要的或主色。 Dynamic Media影像製作提供半自動工具，可從紋理影像中擷取合理的`bgc=`色彩值。

將紋理材質套用至非紋理暈映物件時，如果未指定`bgc=`，則會將`color=`套用為前景色。

## 屬性 {#section-b2db6f147d7f443ba9f671de04c2ef19}

材質屬性。 已被純色和機櫃材料忽略。

## 預設 {#section-de10ef5985ee4ae1ba56d14ba8512b81}

`catalog::BaseColor`如果素材是以目錄專案為基礎，否則`bgc=808080` （中性灰色）。

## 範例 {#section-bf5f0f296bc448ed9d5a84afabcf81e6}

為服裝面料上色，其紋理以RGB色彩120,34,193為主：

`…&src=fabrics/d213.jpg&res=40&bgc=120,34,193&color=140,95,100&…`

## 另請參閱 {#section-de9958dd63a742b4b5d780c59a57da33}

[目錄：：BaseColor](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-basecolor.md#reference-5f02371b1d8e444ab12d2614d9792de8) ， [色彩=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa)
