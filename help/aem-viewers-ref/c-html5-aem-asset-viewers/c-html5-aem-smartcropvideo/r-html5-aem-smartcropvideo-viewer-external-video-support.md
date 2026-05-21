---
title: 外部視訊支援
description: 檢視器支援播放在Dynamic Media Classic或Adobe Experience Manager - Dynamic Media以外託管的視訊。
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 2ab5a083-5995-440a-a9a6-6642277b8a58
TQID: 'https://experienceleague.adobe.com/nLVjtwe8hj5YpMX6M1GKt1Fx-tZK2Qxe1kdWcK8BQPw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 194
ht-degree: 0%

---

# 外部視訊支援{#external-video-support}

檢視器支援播放在Dynamic Media Classic或Adobe Experience Manager - Dynamic Media以外託管的視訊。

支援的外部視訊格式為H.264格式的MP4或HLS資料流的M3U8資訊清單。

檢視器可搭配Dynamic Media Classic或Experience Manager - Dynamic Media視訊或外部視訊使用。 如果檢視器一開始使用Dynamic Media Classic/Dynamic Media視訊，且日後使用此資產型別，則無法使用將外部視訊載入此檢視器 [`setVideo`]
(#reference-85d3422d6ce64a36ac74827120b5a17c)方法。 反之：如果檢視器最初是透過外部視訊載入，則應該只繼續使用外部視訊。

使用外部視訊時，檢視器會忽略playback修飾元的值，並從外部視訊擴充功能中偵測播放型別。 如果外部視訊URL結尾為`.M3U8`，則檢視器會使用HLS播放，否則會使用漸進式播放。
