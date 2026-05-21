---
title: 外部視訊支援
description: 檢視器支援播放在Dynamic Media Classic或Adobe Experience Manager、Dynamic Media以外託管的視訊。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: b592f03b-92ab-47d8-96a6-87982fedc901
TQID: 'https://experienceleague.adobe.com/RCjgY-azk-9IIQyK6-Xz4ju6ev3Otbfs1UFvs3j385U'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 177
ht-degree: 0%

---

# 外部視訊支援{#external-video-support}

檢視器支援播放在Dynamic Media Classic或Adobe Experience Manager、Dynamic Media以外託管的視訊。

支援的外部視訊格式為H.264格式的MP4或HLS資料流的M3U8資訊清單。

檢視器可搭配Dynamic Media Classic或Experience Manager Dynamic Media影片使用，或與外部影片搭配使用。 如果檢視器以Dynamic Media Classic/AEM Dynamic Media視訊開始，就應將其用於這類資產型別。 無法使用[setVideo](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-javascriptapiref/r-html5-aem-video360-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c)方法將外部視訊載入此檢視器，反之亦然。 也就是說，如果檢視器最初是以外部視訊載入，則它只會繼續搭配外部視訊運作。

使用外部視訊時，檢視器會忽略任何playback修飾元的值，並從外部視訊擴充功能中偵測播放型別。 如果外部視訊URL結尾為`.m3u8`，則檢視器會使用HLS播放；否則，會使用漸進式播放。
