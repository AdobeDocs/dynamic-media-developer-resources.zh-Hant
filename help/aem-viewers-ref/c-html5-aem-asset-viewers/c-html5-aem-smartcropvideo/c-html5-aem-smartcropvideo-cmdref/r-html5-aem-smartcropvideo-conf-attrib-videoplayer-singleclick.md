---
description: 智慧型裁切視訊檢視器的設定屬性。
solution: Experience Manager
title: SmartCropVideoPlayer.singleclick
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: 2fd83645-16d4-45ce-8fa8-d97dc254691f
source-git-commit: bdef251dcbb7c135d02813e9fd82e2e5e32300cc
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 5%

---

# SmartCropVideoPlayer.singleclick{#smartcropvideoplayer-singleclick}

智慧型裁切視訊檢視器的設定屬性。

` [SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer.]singleclick= *`none|playPause`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> none|playPause</span> </span> </p> </td> 
   <td colname="col2"> <p> 設定單按/點選的對應以切換播放/暫停。 設定為 <span class="codeph"> 無</span> 停用單按/點選以播放/暫停。 若設為 <span class="codeph"> playPause</span>，則按一下視訊會在播放和暫停視訊之間切換。 在某些裝置上，您可以使用原生控制項。 在這種情況下， <span class="codeph"> 單點按</span> 行為已停用。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-f42369774e2740dcb399626a0e4e930e}

選填。

## 預設 {#section-d016470e92a74f98a18c4ab3489410a5}

`playPause`

## 範例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
singleclick=none
```
