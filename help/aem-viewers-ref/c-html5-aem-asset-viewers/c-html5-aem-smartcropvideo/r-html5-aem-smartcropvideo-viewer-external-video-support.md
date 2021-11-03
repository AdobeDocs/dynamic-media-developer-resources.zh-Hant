---
title: 外部視訊支援
description: 檢視器支援播放在Dynamic Media Classic或Adobe Experience Manager - Dynamic Media以外位置主控的視訊。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: b42e67cb-6959-4eea-8d45-49481e0e9d80
source-git-commit: b6ebc938f55117c4144ff921bed7f8742cf3a8a7
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 0%

---

# 外部視訊支援{#external-video-support}

檢視器支援播放在Dynamic Media Classic或Adobe Experience Manager - Dynamic Media以外位置主控的視訊。

支援的外部視訊格式為H.264格式的MP4或HLS資料流的M3U8資訊清單。

檢視器可運作Dynamic Media Classic或Experience Manager- Dynamic Media影片或搭配外部影片。 如果檢視器以Dynamic Media Classic/Dynamic Media影片開頭，請將其與未來的這類資產類型搭配使用，則無法使用將外部影片載入至此檢視器中 [`setVideo`]
(../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-javascriptapiref/r-html5-aem-smartcropvideo-viewer-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c)方法。 副詞：如果檢視器最初載入的是外部視訊，則應該只持續使用外部視訊。

使用外部視訊時，檢視器會忽略播放修飾元的值，並從外部視訊擴充功能偵測播放類型。 如果外部視訊URL的結尾為 `.M3U8` 檢視器使用HLS播放，否則會使用漸進式播放。
