---
title: VideoTime.timepattern
description: 智慧型裁切視訊檢視器的設定屬性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: b63818e2-8da0-4965-b7d6-5ecd7ab5cdca
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 2%

---

# VideoTime.timepattern{#videotime-timepattern}

智慧型裁切視訊檢視器的設定屬性。

`[VideoTime.|<containerId>_videoTime.]timepattern=[h:]m|mm:s|ss`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h：]m|mm：s|ss</span> </p> </td> 
   <td colname="col2"> <p> 設定控制列中顯示的時間模式，其中<span class="codeph"> h</span>是小時，<span class="codeph"> m</span>是分鐘，<span class="codeph"> s</span>是秒。 </p> <p>用於每個時間單位的字母數目決定該單位要顯示的位數。 如果數字不符合指定的位數，則會在後續單位中顯示對等值。 </p> <p>例如，如果目前的影片時間為67分5秒，則時間模式<span class="codeph"> m：ss</span>會顯示為67:05。 如果指定的時間模式為<span class="codeph"> h:mm:s</span>，則相同的時間會顯示為1:07:5。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-f42369774e2740dcb399626a0e4e930e}

選擇性.

## 預設 {#section-d016470e92a74f98a18c4ab3489410a5}

`m:ss`

## 範例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
timepattern=h:mm:ss
```
