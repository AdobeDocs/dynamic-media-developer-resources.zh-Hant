---
title: VideoPlayer.initialbitrate
description: 視頻查看器的配置屬性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 83f2af31-e2dc-430c-b9ae-563cdcd20954
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 3%

---

# VideoPlayer.initialbitrate{#videoplayer-initialbitrate}

視頻查看器的配置屬性。

` [VideoPlayer.|<containerId>_videoPlayer.]initialbitrate= *`值`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 值 </span> </p> </td> 
   <td colname="col2"> <p>設定用於案頭上視頻初始回放的視頻比特率（千位/秒或千位/秒）。 </p> <p>如果此比特率值在自適應視頻集中不存在，則視頻播放器將啟動具有下一個最低比特率的視頻。 </p> <p>如果設定為 <span class="codeph"> 0 </span>，視頻播放器從最低可能比特率開始。 僅適用於不支援HTML5 HLS視頻（Windows 10上的Firefox、Chrome和Internet Explorer 11瀏覽器）的系統，並且當播放模式設定為 <span class="codeph"> 自動 </span>。 </p> </td> 
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
