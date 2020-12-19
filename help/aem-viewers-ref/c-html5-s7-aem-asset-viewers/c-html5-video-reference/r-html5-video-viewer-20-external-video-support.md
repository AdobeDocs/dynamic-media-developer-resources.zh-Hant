---
description: 檢視器支援播放Scene7 Publishing System或AEM Dynamic Media以外位置代管的視訊。
seo-description: 檢視器支援播放Scene7 Publishing System或AEM Dynamic Media以外位置代管的視訊。
seo-title: 外部視訊支援
solution: Experience Manager
title: 外部視訊支援
topic: Dynamic media
uuid: 24739a5a-3a5d-49b8-9a15-bcf3a95fc192
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 0%

---


# 外部視訊支援{#external-video-support}

檢視器支援播放Scene7 Publishing System或AEM Dynamic Media以外位置代管的視訊。

外部視訊支援的格式為H.264格式的MP4或HLS串流的M3U8資訊清單。

檢視器可以使用Scene7或Dynamic Media視訊，或與外部視訊搭配使用。 如果檢視器以Scene7/Dynamic Media視訊開頭，請繼續將它與此類資產類型搭配使用，則無法使用[ `setVideo`](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c)方法將外部視訊載入此檢視器。 副詞：如果檢視器最初載入外部視訊，則應僅繼續使用外部視訊。

使用外部視訊時，檢視器會忽略播放修飾元的值，並偵測來自外部視訊擴充功能的播放類型。 如果外部視訊URL以。m3u8結尾，檢視器會使用HLS播放，否則會使用漸進式播放。
