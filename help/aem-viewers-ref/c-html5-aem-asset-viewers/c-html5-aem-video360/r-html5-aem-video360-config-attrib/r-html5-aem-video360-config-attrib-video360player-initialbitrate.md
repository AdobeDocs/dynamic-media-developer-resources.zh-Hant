---
description: Video360檢視器的設定屬性。
seo-description: Video360檢視器的設定屬性。
seo-title: Video360Player.initialbitrate
solution: Experience Manager
title: Video360Player.initialbitrate
topic: Dynamic media
uuid: a23fa941-6dd2-41c0-aca9-06f0cdb027b1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 8%

---


# Video360Player.initialbitrate{#video-player-initialbitrate}

Video360檢視器的設定屬性。

` [Video360Player.|<containerId>_video360Player.]initialbitrate= *`值`*`

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

