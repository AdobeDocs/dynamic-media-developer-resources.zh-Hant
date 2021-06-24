---
description: 視訊檢視器的設定屬性。
solution: Experience Manager
title: VideoTime.timepattern
feature: Dynamic Media Classic，檢視器， SDK/API，影片
role: Developer,Business Practitioner
exl-id: 1fe2876c-c59a-4e0c-b429-34cc3244d920
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 3%

---

# VideoTime.timepattern{#videotime-timepattern}

視訊檢視器的設定屬性。

`[VideoTime.|<containerId>_videoTime.]timepattern=[h:]m|mm:s|ss`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> 設定控制欄中顯示的時間模式，其中<span class="codeph"> h</span>為小時，<span class="codeph"> m</span>為分鐘，而<span class="codeph"> s</span>為秒。 </p> <p>每個時間單位使用的字母數決定單位要顯示的位數。 如果數字不能滿足給定位數，則等效值將以後續單位顯示。 </p> <p>例如，如果目前的影片時間是67分鐘5秒，則時間模式<span class="codeph"> m:ss</span>顯示為67:05。 如果給定的時間模式為<span class="codeph"> h:mm:s</span>，則將該時間顯示為1:07:5。 </p> </td> 
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
