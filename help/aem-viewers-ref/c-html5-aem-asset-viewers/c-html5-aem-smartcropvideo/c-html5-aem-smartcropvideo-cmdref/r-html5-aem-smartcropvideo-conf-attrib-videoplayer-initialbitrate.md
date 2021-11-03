---
description: 智慧型裁切視訊檢視器的設定屬性。
solution: Experience Manager
title: SmartCropVideoPlayer.initialbitrate
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: 83f2af31-e2dc-430c-b9ae-563cdcd20954
source-git-commit: bdef251dcbb7c135d02813e9fd82e2e5e32300cc
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 3%

---

# SmartCropVideoPlayer.initialbitrate{#smartcropvideoplayer-initialbitrate}

視訊檢視器的設定屬性。

` [SmartCropVideoPlayer.|<containerId>_videoPlayer.]initialbitrate= *`value`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> value </span> </p> </td> 
   <td colname="col2"> <p>設定用於在案頭上初始播放視頻的視頻的視頻位元速率（以千位/秒為單位）或每秒位元組數。 </p> <p>如果此位元速率值在適用性視訊集中不存在，則視訊播放器會啟動位元速率下一個最低的視訊。 </p> <p>若設為 <span class="codeph"> 0 </span> 視訊播放器從最低的位元速率開始。 僅適用於不支援HTML5 HLS視訊（在Windows 10上為Firefox、Chrome和Internet Explorer 11瀏覽器）的系統，以及當播放模式設為 <span class="codeph"> 自動 </span>. </p> </td> 
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
