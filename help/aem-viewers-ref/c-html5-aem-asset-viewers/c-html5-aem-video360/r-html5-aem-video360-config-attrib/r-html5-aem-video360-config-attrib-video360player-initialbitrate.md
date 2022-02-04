---
title: Video360Player.initialbitrate
description: Video360查看器的配置屬性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: f36eb82a-e545-4063-8bc4-6315ed17758f
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 7%

---

# Video360Player.initialbitrate{#video-player-initialbitrate}

Video360查看器的配置屬性。

` [Video360Player.|<containerId>_video360Player.]initialbitrate= *`值`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 值</span> </p> </td> 
   <td colname="col2"> <p> 設定用於案頭上視頻初始回放的視頻比特率（千比特/秒或kbps）。 </p> <p>如果自適應視頻集中不存在此比特率值，則視頻播放器從具有下一個較低比特率的視頻開始。 </p> <p>如果設定為 <span class="codeph"> 0</span>，視頻播放器從最低可能比特率開始。 </p> <p>僅適用於不支援HTML5 HLS視頻的系統（如Windows 10上的Firefox、Chrome和Internet Explorer 11瀏覽器），並且播放模式設定為「自動」時。 </p> </td> 
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
