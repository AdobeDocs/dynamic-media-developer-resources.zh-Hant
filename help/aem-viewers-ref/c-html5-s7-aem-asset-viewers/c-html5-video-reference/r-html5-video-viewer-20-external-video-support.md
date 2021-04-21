---
description: 檢視器支援在Dynamic Media經典或Dynamic Media以外播放AEM視訊。
solution: Experience Manager
title: 外部視訊支援
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 0%

---


# 外部視訊支援{#external-video-support}

檢視器支援在Dynamic Media經典或Dynamic Media以外播放AEM視訊。

外部視訊支援的格式為H.264格式的MP4或HLS串流的M3U8資訊清單。

檢視器可以使用Dynamic Media經典或AEMDynamic Media視訊，或外部視訊。 如果檢視器以Dynamic Media經典/Dynamic Media視訊開頭，請繼續將它與此類資產類型搭配使用，則無法使用[ `setVideo`](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c)方法將外部視訊載入此檢視器。 副詞：如果檢視器最初載入外部視訊，則應僅繼續使用外部視訊。

使用外部視訊時，檢視器會忽略播放修飾元的值，並偵測來自外部視訊擴充功能的播放類型。 如果外部視訊URL以。m3u8結尾，檢視器會使用HLS播放，否則會使用漸進式播放。
