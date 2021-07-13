---
description: Video360查看器的配置屬性。
solution: Experience Manager
title: Video360Player.initialbitrate
feature: Dynamic Media Classic，檢視器，SDK/API,360 VR影片
role: Developer,User
exl-id: f36eb82a-e545-4063-8bc4-6315ed17758f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 6%

---

# Video360Player.initialbitrate{#video-player-initialbitrate}

Video360查看器的配置屬性。

` [Video360Player.|<containerId>_video360Player.]initialbitrate= *`value`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> value</span> </p> </td> 
   <td colname="col2"> <p> 設定用於案頭上視頻初始播放的視頻位元速率（以每秒kbits或每秒kbps為單位）。 </p> <p>如果此位元速率值在適用性視訊集中不存在，視訊播放器會從下一個位元速率較低的視訊開始。 </p> <p>如果設為<span class="codeph"> 0</span>，視訊播放器會從最低的位元速率開始。 </p> <p>僅適用於不支援HTML5 HLS視訊的系統（例如Windows 10上的Firefox、Chrome和Internet Explorer 11瀏覽器），以及當播放模式設為自動時。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-f42369774e2740dcb399626a0e4e930e}

選填。

## 預設 {#section-d016470e92a74f98a18c4ab3489410a5}

`1400`

## 範例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
initialbitrate=600
```
