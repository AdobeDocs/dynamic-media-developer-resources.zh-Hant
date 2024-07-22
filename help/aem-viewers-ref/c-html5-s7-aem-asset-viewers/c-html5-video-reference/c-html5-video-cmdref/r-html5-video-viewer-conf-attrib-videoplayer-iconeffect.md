---
title: VideoPlayer.iconeffect
description: 視訊檢視器的設定屬性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: b283b495-ee28-4f9d-ad4d-b14ac2f9a1a2
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 2%

---

# VideoPlayer.iconeffect{#videoplayer-iconeffect}

視訊檢視器的設定屬性。

` [VideoPlayer.|<containerId>_videoPlayer.]iconeffect= *`0|1`*[, *`計數`*][, *`淡化`*][, *`自動隱藏`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 0|1</span> </span> </p> </td> 
   <td colname="col2"> <p> 啟用IconEffect，以便在視訊暫停時顯示在視訊上方。 在某些裝置上，會使用原生控制項。 在這種情況下，會忽略<span class="codeph"> iconeffect</span>修飾元。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">計數</span> </span> </p> </td> 
   <td colname="col2"> <p> 指定IconEffect出現和重新出現的最大次數。 值為<span class="codeph"> -1</span>表示圖示會無限期地重新出現。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">淡化</span> </span> </p> </td> 
   <td colname="col2"> <p> 指定顯示或隱藏動畫的持續時間（秒）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">自動隱藏</span> </span> </p> </td> 
   <td colname="col2"> <p> 設定IconEffect在自動隱藏前保持可見的秒數。 亦即，淡入動畫完成後的時間，以及淡出動畫開始前的時間。 設定為<span class="codeph"> 0</span>會停用自動隱藏行為。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-f42369774e2740dcb399626a0e4e930e}

選擇性.

## 預設 {#section-d016470e92a74f98a18c4ab3489410a5}

`1,-1,0.3,0`

## 範例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
iconeffect=0
```
