---
title: 外部視頻支援
description: 觀眾支援在Dynamic Media Classic或Adobe Experience Manager以外播放視頻 — Dynamic Media。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: b42e67cb-6959-4eea-8d45-49481e0e9d80
source-git-commit: 11acb9151d3ea247eecde3cfbbd295a95c10829c
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---

# 外部視頻支援{#external-video-support}

觀眾支援在Dynamic Media Classic或Adobe Experience Manager以外播放視頻 — Dynamic Media。

外部視頻支援的格式為H.264格式的MP4或HLS流的M3U8清單。

觀看者可以使用Dynamic Media Classic或Experience Manager-Dynamic Media視頻或外部視頻。 如果查看者以Dynamic Media Classic/Dynamic Media視頻開頭，請將其與此類資產類型一起使用，則無法使用 [ `setVideo`](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c) 的雙曲餘切值。 還有副詞：如果查看器最初載入了外部視頻，則它應該只處理外部視頻。

使用外部視頻時，查看器會忽略回放修飾符的值，並從外部視頻擴展中檢測回放類型。 如果外部視頻URL以 `.m3u8` 查看器正在使用HLS回放，否則將使用逐步回放。
