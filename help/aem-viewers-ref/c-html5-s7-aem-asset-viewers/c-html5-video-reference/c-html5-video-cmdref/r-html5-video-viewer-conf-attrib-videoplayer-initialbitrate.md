---
description: 視訊檢視器的設定屬性。
solution: Experience Manager
title: VideoPlayer.initialbitrate
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 3%

---


# VideoPlayer.initialbitrate{#videoplayer-initialbitrate}

視訊檢視器的設定屬性。

` [VideoPlayer.|<containerId>_videoPlayer.]initialbitrate= *`值`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 值  </span> </p> </td> 
   <td colname="col2"> <p>設定用於在桌上型電腦上播放視訊的視訊位元速率（以千位／秒為單位）或kbps。 </p> <p>如果此位元速率值不存在於最適化視訊集中，則視訊播放器會啟動位元速率下一個最低的視訊。 </p> <p>如果設為<span class="codeph"> 0 </span>，則視訊播放器會從最低位元速率開始。 僅適用於不支援HTML5 HLS視訊的系統（Windows 10上的Firefox、Chrome和Internet Explorer 11瀏覽器），以及當播放模式設為<span class="codeph">自動</span>時。 </p> </td> 
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

