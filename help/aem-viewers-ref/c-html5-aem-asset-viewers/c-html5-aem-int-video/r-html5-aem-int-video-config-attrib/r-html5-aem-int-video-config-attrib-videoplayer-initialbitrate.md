---
description: 互動式視訊檢視器的設定屬性。
seo-description: 互動式視訊檢視器的設定屬性。
seo-title: VideoPlayer.initialbitrate
solution: Experience Manager
title: VideoPlayer.initialbitrate
topic: Dynamic Media
uuid: 251ab7d2-a0b5-4658-a2b8-6b39dd93dd5b
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 3%

---


# VideoPlayer.initialbitrate{#videoplayer-initialbitrate}

互動式視訊檢視器的設定屬性。

` [VideoPlayer.|<containerId>_videoPlayer.]initialbitrate= *`值`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 值</span> </p> </td> 
   <td colname="col2"> <p> 設定用於在桌上型電腦上初始播放視訊的視訊位元速率（以每秒k位元或kbps為單位）。 </p> <p>如果此位元速率值不存在於最適化視訊集中，視訊播放器會從具有下一個較低位元速率的視訊開始。 </p> <p>如果設為<span class="codeph"> 0</span>，則視訊播放器會從最低位元速率開始。 </p> <p>僅適用於不支援HTML5 HLS視訊的系統（例如Windows 10上的Firefox、Chrome和Internet Explorer 11瀏覽器），以及當播放模式設為「自動」時。 </p> </td> 
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

