---
title: VideoPlayer.singleclick
description: Interactive Video Viewer的配置屬性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 038640c7-ae8c-43e0-979b-6010bb5e40fb
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 4%

---

# VideoPlayer.singleclick{#videoplayer-singleclick}

Interactive Video Viewer的配置屬性。

`[VideoPlayer.|<containerId>_videoPlayer.]singleclick=none|playPause`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 無|播放暫停</span> </p> </td> 
   <td colname="col2"> <p> 配置按一下/點擊的映射以切換播放/暫停。 設定為 <span class="codeph"> 無</span> 禁用按一下/點擊以播放/暫停。 如果設定為 <span class="codeph"> 播放暫停</span>，然後選擇視頻在播放和暫停視頻之間切換。 在某些設備上，可以使用本機控制項。 在這種情況下， <span class="codeph"> 按一下</span> 行為已禁用。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

選擇性.

## 預設 {#section-71fb773f814649b2885aefee68073641}

`playPause`

## 範例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
singleclick=none
```
