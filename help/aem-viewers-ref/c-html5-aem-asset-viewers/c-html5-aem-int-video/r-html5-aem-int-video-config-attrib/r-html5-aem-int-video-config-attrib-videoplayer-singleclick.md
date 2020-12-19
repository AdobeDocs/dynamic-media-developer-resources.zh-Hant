---
description: 互動式視訊檢視器的設定屬性。
seo-description: 互動式視訊檢視器的設定屬性。
seo-title: VideoPlayer.singleclick
solution: Experience Manager
title: VideoPlayer.singleclick
topic: Dynamic media
uuid: 5b387eb6-1e09-4506-beea-3f1cf337cb9d
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 5%

---


# VideoPlayer.singleclick{#videoplayer-singleclick}

互動式視訊檢視器的設定屬性。

`[VideoPlayer.|<containerId>_videoPlayer.]singleclick=none|playPause`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|playPause</span> </p> </td> 
   <td colname="col2"> <p> 設定單鍵／點選的對應，以切換播放／暫停。 設為<span class="codeph"> none</span>會停用單鍵／點選以播放／暫停。 如果設為<span class="codeph"> playPause</span>，則按一下視訊會在播放和暫停視訊之間切換。 在某些裝置上，您可以使用原生控制項。 在這種情況下，<span class="codeph">單點按鍵行為將被禁用。</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

選填。

## 預設 {#section-71fb773f814649b2885aefee68073641}

`playPause`

## 範例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
singleclick=none
```

