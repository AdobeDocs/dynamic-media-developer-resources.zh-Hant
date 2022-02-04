---
title: VideoPlayer.singleclick
description: 視頻查看器的配置屬性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 2fd83645-16d4-45ce-8fa8-d97dc254691f
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 5%

---

# VideoPlayer.singleclick{#videoplayer-singleclick}

視頻查看器的配置屬性。

` [VideoPlayer.|<containerId>_videoPlayer.]singleclick= *`無|播放暫停`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 無|播放暫停</span> </span> </p> </td> 
   <td colname="col2"> <p> 配置按一下/點擊的映射以切換播放/暫停。 設定為 <span class="codeph"> 無</span> 禁用按一下/點擊以播放/暫停。 如果設定為 <span class="codeph"> 播放暫停</span>，按一下視頻在播放和暫停視頻之間切換。 在某些設備上，可以使用本機控制項。 在這種情況下， <span class="codeph"> 按一下</span> 行為已禁用。 </p> </td> 
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
