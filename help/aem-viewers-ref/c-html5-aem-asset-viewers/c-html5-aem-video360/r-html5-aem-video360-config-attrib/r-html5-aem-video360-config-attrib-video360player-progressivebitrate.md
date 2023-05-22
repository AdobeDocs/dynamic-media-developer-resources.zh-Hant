---
title: Video360Player.progressivebitrate
description: Video360查看器的配置屬性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: a253ef01-19ae-4de4-a4fc-b10b28e72c00
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 7%

---

# Video360Player.progressivebitrate{#video-player-progressivebitrate}

Video360查看器的配置屬性。

` [Video360Player.|<containerId>_video360Player.]progressivebitrate= *`值`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 值</span> </p> </td> 
   <td colname="col2"> <p> 指定在當前系統不支援自適應視頻回放時從自適應視頻集播放的所需視頻比特率（千比特/秒或千比特）。 </p> <p>該元件以最接近（但不超過）的比特率提取視頻流到指定值。 如果自適應視頻集中的所有視頻流的質量都高於指定值，則邏輯選擇質量最低的比特率。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-f42369774e2740dcb399626a0e4e930e}

選擇性.

## 預設 {#section-d016470e92a74f98a18c4ab3489410a5}

`700`

## 範例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
progressivebitrate=600
```
