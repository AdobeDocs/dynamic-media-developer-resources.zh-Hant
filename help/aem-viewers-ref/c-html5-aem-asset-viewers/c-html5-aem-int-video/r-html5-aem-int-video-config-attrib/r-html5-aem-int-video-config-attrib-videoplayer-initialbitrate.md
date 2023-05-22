---
title: VideoPlayer.initialbitrate
description: Interactive Video Viewer的配置屬性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 75ee2c74-21c4-41b6-9d0f-15aa8432f177
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 2%

---

# VideoPlayer.initialbitrate{#videoplayer-initialbitrate}

Interactive Video Viewer的配置屬性。

` [VideoPlayer.|<containerId>_videoPlayer.]initialbitrate= *`值`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 值</span> </p> </td> 
   <td colname="col2"> <p> 設定用於案頭上視頻初始回放的視頻比特率（千比特/秒或kbps）。 </p> <p>如果自適應視頻集中不存在此比特率值，則視頻播放器從具有下一個較低比特率的視頻開始。 </p> <p>如果設定為 <span class="codeph"> 0</span>，視頻播放器從最低可能比特率開始。 </p> <p>僅適用於不支援HTML5 HLS視頻的系統（如Windows 10上的Firefox、Chrome和Internet Explorer 11瀏覽器），並且播放模式設定為「自動」時。 </p> </td> 
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
