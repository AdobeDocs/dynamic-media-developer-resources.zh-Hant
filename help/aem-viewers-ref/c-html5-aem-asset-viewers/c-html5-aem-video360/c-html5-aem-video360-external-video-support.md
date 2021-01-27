---
description: 檢視器支援播放SPS或AEM Dynamic Media以外位置代管的視訊。
seo-description: 檢視器支援播放SPS或AEM Dynamic Media以外位置代管的視訊。
seo-title: 外部視訊支援
solution: Experience Manager
title: 外部視訊支援
topic: Dynamic Media
uuid: 2e9f1c54-627f-4462-ae85-8a5ca1d09762
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 0%

---


# 外部視訊支援{#external-video-support}

檢視器支援播放SPS或AEM Dynamic Media以外位置代管的視訊。

外部視訊支援的格式為H.264格式的MP4或HLS串流的M3U8資訊清單。

檢視器可以使用Dynamic Media Classic或AEM Dynamic Media視訊，或與外部視訊搭配使用。 如果檢視器以Dynamic Media Classic/AEM Dynamic Media視訊開頭，則應將它與此類資產類型搭配使用。 無法使用[setVideo](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-javascriptapiref/r-html5-aem-video360-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c)方法將外部視訊載入此檢視器，反之亦然。 也就是說，如果檢視器最初載入外部視訊，則只能繼續使用外部視訊。

使用外部視訊時，檢視器會忽略任何播放修飾元的值，並偵測來自外部視訊擴充功能的播放類型。 如果外部視訊URL結尾為`.m3u8`，檢視器會使用HLS播放；否則，會使用漸進式播放。
