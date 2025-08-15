---
title: VideoPlayer.initialbitrate
description: 互動式視訊檢視器的設定屬性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 75ee2c74-21c4-41b6-9d0f-15aa8432f177
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 2%

---

# VideoPlayer.initialbitrate{#videoplayer-initialbitrate}

互動式視訊檢視器的設定屬性。

` [VideoPlayer.|<containerId>_videoPlayer.]initialbitrate= *`值`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">值</span> </p> </td> 
   <td colname="col2"> <p> 設定在案頭上初始播放視訊時使用的視訊位元速率（以每秒KB或kbps為單位）。 </p> <p>如果「自我調整視訊集」中不存在此位元速率值，則視訊播放器會從擁有次低位元速率的視訊開始。 </p> <p>如果設為<span class="codeph"> 0</span>，視訊播放器會從最低的位元速率開始。 </p> <p>僅適用於不具備HTML5 HLS視訊原生支援的系統(例如Windows 10上的Firefox、Chrome和Internet Explorer 11瀏覽器)，以及當播放模式設定為auto時。 </p> </td> 
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
