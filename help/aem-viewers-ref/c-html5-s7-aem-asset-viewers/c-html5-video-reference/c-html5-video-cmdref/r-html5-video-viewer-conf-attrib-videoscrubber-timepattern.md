---
title: VideoScrubber.timepattern
description: 視頻查看器的配置屬性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: e0956a0b-4d82-475f-8990-8b059014233a
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 3%

---

# VideoScrubber.timepattern{#videoscrubber-timepattern}

視頻查看器的配置屬性。

`[VideoScrubber.|<containerId>_videoScrubber.]timepattern=[h:]m|mm:s|ss`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> 設定時間氣泡中顯示的時間的模式，其中 <span class="codeph"> h</span> 是小時， <span class="codeph"> 米</span> 是分鐘 <span class="codeph"> s</span> 秒。 </p> <p>每個時間單位使用的字母數決定單位顯示的位數。 如果數字不能容納給定數字，則在後續單位中顯示等效值。 </p> <p>例如，如果當前電影時間是67分5秒，則時間模式 <span class="codeph"> m:ss</span> 顯示為67:05。 同時顯示為1:07:5如果給定的時間模式 <span class="codeph"> h:mm:s</span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-f42369774e2740dcb399626a0e4e930e}

選填。

## 預設 {#section-d016470e92a74f98a18c4ab3489410a5}

`m:ss`

## 範例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
timepattern=h:mm:ss
```
