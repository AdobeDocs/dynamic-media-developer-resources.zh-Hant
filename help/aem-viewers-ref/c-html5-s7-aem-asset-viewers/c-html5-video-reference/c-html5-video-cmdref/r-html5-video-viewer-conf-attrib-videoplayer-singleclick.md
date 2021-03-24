---
description: 視訊檢視器的設定屬性。
solution: Experience Manager
title: VideoPlayer.singleclick
feature: Dynamic Media經典，檢視器，SDK/API，視訊
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 5%

---


# VideoPlayer.singleclick{#videoplayer-singleclick}

視訊檢視器的設定屬性。

` [VideoPlayer.|<containerId>_videoPlayer.]singleclick= *`none|playPause`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> none|playPause</span> </span> </p> </td> 
   <td colname="col2"> <p> 設定單鍵／點選的對應，以切換播放／暫停。 設為<span class="codeph"> none</span>會停用單鍵／點選以播放／暫停。 如果設為<span class="codeph"> playPause</span>，按一下視訊會在播放和暫停視訊之間切換。 在某些裝置上，您可以使用原生控制項。 在這種情況下，<span class="codeph"> syncolick</span>行為會停用。 </p> </td> 
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

