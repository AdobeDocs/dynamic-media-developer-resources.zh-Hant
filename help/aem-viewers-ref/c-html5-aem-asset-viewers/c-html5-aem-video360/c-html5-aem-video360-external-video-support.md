---
title: 外部視頻支援
description: 觀眾支援在Dynamic Media Classic或Dynamic MediaAdobe Experience Manager以外播放視頻。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: b592f03b-92ab-47d8-96a6-87982fedc901
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 0%

---

# 外部視頻支援{#external-video-support}

觀眾支援在Dynamic Media Classic或Dynamic MediaAdobe Experience Manager以外播放視頻。

外部視頻支援的格式為H.264格式的MP4或HLS流的M3U8清單。

觀看者可以使用Dynamic Media Classic或Experience ManagerDynamic Media視頻或外部視頻。 如果查看器以Dynamic Media Classic/AEMDynamic Media視頻開頭，則應將其用於後續的此類資產類型。 無法使用 [setVideo](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-javascriptapiref/r-html5-aem-video360-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c) 方法，反之。 即，如果查看器最初載入了外部視頻，則它只能繼續處理外部視頻。

使用外部視頻時，查看器會忽略任何播放修飾符的值，並從外部視頻擴展檢測播放類型。 如果外部視頻URL以 `.m3u8`，查看器正在使用HLS回放；否則，使用漸進式回放。
