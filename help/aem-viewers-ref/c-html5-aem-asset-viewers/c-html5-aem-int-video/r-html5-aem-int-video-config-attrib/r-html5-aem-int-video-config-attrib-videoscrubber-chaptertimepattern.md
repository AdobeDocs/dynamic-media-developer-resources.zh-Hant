---
description: 互動式視訊檢視器的設定屬性。
solution: Experience Manager
title: VideoScrubber.chaptertimepattern
feature: Dynamic Media Classic，檢視器， SDK/API，互動式影片
role: Developer,User
exl-id: 93c1d38c-1f45-4794-8084-f520f9caf257
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 3%

---

# VideoScrubber.chaptertimepattern{#videoscrubber-chaptertimepattern}

互動式視訊檢視器的設定屬性。

`[VideoScrubber.|<containerId>_videoScrubber.]chaptertimepattern=[h:]m|mm:s|ss`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> 設定在章節標籤標題列中顯示的時間模式，其中<span class="codeph"> h</span>代表小時，<span class="codeph"> m</span>代表分鐘，<span class="codeph"> s</span>代表秒。 </p> <p>每個時間單位使用的字母數決定單位要顯示的位數。 如果數字不能滿足給定位數，則等效值將以後續單位顯示。 </p> <p>例如，如果目前的影片時間是67分鐘5秒，則<span class="codeph"> m:ss</span>的時間模式會顯示為67:05。 如果時間模式為<span class="codeph">h:mm:s</span>，則將同一時間顯示為1:07:5。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

選填。

## 預設 {#section-71fb773f814649b2885aefee68073641}

`m:ss`

## 範例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
chaptertimepattern=h:mm:ss
```
