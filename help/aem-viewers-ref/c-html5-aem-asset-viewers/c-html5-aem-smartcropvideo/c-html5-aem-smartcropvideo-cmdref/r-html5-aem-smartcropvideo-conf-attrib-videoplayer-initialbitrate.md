---
title: SmartCropVideoPlayer.initialbitrate
description: 智慧型裁切視訊檢視器的設定屬性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 4fc4fefa-b094-4e2e-b8ec-a439f8a1a56c
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 2%

---

# SmartCropVideoPlayer.initialbitrate{#smartcropvideoplayer-initialbitrate}

視訊檢視器的設定屬性。

` [SmartCropVideoPlayer.|<containerId>_videoPlayer.]initialbitrate= *`值`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">值</span> </p> </td> 
   <td colname="col2"> <p>設定在桌上型電腦上初始播放視訊時使用的視訊位元速率（以每秒KB或kbps為單位）。 </p> <p>如果此位元速率值不存在最適化視訊集中，則視訊播放器會啟動具有下一個最低位元速率的視訊。 </p> <p>如果設為<span class="codeph"> 0 </span>，視訊播放器會從最低的位元速率開始。 僅適用於不具備HTML5 HLS視訊原生支援的系統(Windows 10上的Firefox、Chrome和Internet Explorer 11瀏覽器)，以及當播放模式設定為<span class="codeph">自動</span>時。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-f42369774e2740dcb399626a0e4e930e}

選擇性.

## 預設 {#section-d016470e92a74f98a18c4ab3489410a5}

`1400`

## 範例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
initialbitrate=600
```
