---
title: VideoPlayer.singleclick
description: 互動式視訊檢視器的設定屬性。
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

互動式視訊檢視器的設定屬性。

`[VideoPlayer.|<containerId>_videoPlayer.]singleclick=none|playPause`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|playPause</span> </p> </td> 
   <td colname="col2"> <p> 設定按一下/點選以切換播放/暫停的對應。 設定為<span class="codeph"> none</span>會停用按一下/點選以播放/暫停。 若設為<span class="codeph"> playPause</span>，則選取視訊可在播放和暫停視訊之間切換。 在某些裝置上，您可以使用原生控制項。 在此情況下，<span class="codeph"> singleclick</span>行為已停用。 </p> </td> 
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
