---
description: 檢視器支援播放在Dynamic Media Classic或AEM Dynamic Media以外位置托管的視訊。
solution: Experience Manager
title: 外部視訊支援
feature: Dynamic Media Classic，檢視器，SDK/API,360 VR影片
role: Developer,Business Practitioner
exl-id: b592f03b-92ab-47d8-96a6-87982fedc901
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 0%

---

# 外部視訊支援{#external-video-support}

檢視器支援播放在Dynamic Media Classic或AEM Dynamic Media以外位置托管的視訊。

支援的外部視訊格式為H.264格式的MP4或HLS資料流的M3U8資訊清單。

檢視器可運作Dynamic Media Classic或AEM Dynamic Media影片，或搭配外部影片。 如果檢視器以Dynamic Media Classic/AEM Dynamic Media影片開頭，則應與日後的這類資產類型搭配使用。 無法使用[setVideo](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-javascriptapiref/r-html5-aem-video360-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c)方法將外部視訊載入到此檢視器，反之亦然。 也就是說，如果檢視器最初載入外部視訊，則只會繼續處理外部視訊。

使用外部視訊時，檢視器會忽略任何播放修飾元的值，並從外部視訊擴充功能偵測播放類型。 如果外部視訊URL的結尾是`.m3u8`，檢視器會使用HLS播放；否則，會使用漸進式播放。
