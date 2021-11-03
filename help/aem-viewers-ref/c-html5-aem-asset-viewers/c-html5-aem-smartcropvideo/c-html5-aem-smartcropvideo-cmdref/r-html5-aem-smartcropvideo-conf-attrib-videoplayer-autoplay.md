---
title: SmartCropVideoPlayer.autoplay
description: 智慧型裁切視訊檢視器的設定屬性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: ec0bb98a-7c0b-4ed7-b47d-7c103b6a5943
source-git-commit: b6ebc938f55117c4144ff921bed7f8742cf3a8a7
workflow-type: tm+mt
source-wordcount: '42'
ht-degree: 14%

---

# SmartCropVideoPlayer.autoplay{#smartcropvideoplayer-autoplay}

智慧型裁切視訊檢視器的設定屬性。

` [SmartCropVideoPlayer.|<containerId>_videoPlayer.]autoplay= *`0 | 1`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 0|1</span> </span> </p> </td> 
   <td colname="col2"> <p> 指出檢視器是否在載入時開始播放視訊。 某些系統（例如某些行動裝置）不支援AutoPlay。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-f42369774e2740dcb399626a0e4e930e}

選填。

## 預設 {#section-d016470e92a74f98a18c4ab3489410a5}

`0`

## 範例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
autoplay=1
```
