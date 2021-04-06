---
description: Video360檢視器的設定屬性。
solution: Experience Manager
title: VideoTime.timepattern
feature: Dynamic Media經典，檢視器，SDK/API,360 VR視訊
role: 開發人員，商業從業人員
exl-id: a3a4f3f9-b6ef-4ee2-b006-578b743698ad
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 3%

---

# VideoTime.timepattern{#videotime-timepattern}

Video360檢視器的設定屬性。

`[VideoTime.|<containerId>_videoTime.]timepattern=[h:]m|mm:s|ss`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> 設定在控制欄中顯示的時間模式，其中<span class="codeph"> h</span>是小時，<span class="codeph"> m</span>是分鐘，<span class="codeph"> s</span>是秒。 </p> <p>每個時間單位使用的字母數決定單位要顯示的位數。 如果數字不能與給定數字匹配，則等效值將顯示在後續單位中。 </p> <p>例如，如果目前的影片時間是67分5秒，則時間模式<span class="codeph"> m:ss</span>會顯示為67:05。 如果給定時間模式為<span class="codeph"> h:mm:s</span>，則顯示相同時間。 </p> </td> 
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
