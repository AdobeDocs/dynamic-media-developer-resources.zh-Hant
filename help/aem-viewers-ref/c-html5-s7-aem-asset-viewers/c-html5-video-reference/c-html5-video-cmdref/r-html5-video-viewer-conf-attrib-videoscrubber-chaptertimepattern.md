---
description: 視訊檢視器的設定屬性。
seo-description: 視訊檢視器的設定屬性。
seo-title: VideoScrubber.chaptertimepattern
solution: Experience Manager
title: VideoScrubber.chaptertimepattern
topic: Dynamic media
uuid: 75338fa6-83ab-4cb8-babf-e958f97c1b6e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# VideoScrubber.chaptertimepattern{#videoscrubber-chaptertimepattern}

視訊檢視器的設定屬性。

`[VideoScrubber.|<containerId>_videoScrubber.]chaptertimepattern=[h:]m|mm:s|ss`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> 設定在視訊章節標籤標題列中顯示的時間模式，其中 <span class="codeph"> h</span> 為小時、 <span class="codeph"> m</span> 為分鐘 <span class="codeph"> 和</span> s為秒。 </p> <p>每個時間單位使用的字母數決定單位要顯示的位數。 如果數字不能與給定數字匹配，則等效值將顯示在後續單位中。 </p> <p>例如，如果目前的影片時間是67分5秒，時間模式 <span class="codeph"> m:ss</span> 會顯示為67:05。 如果給定時間模式為 <span class="codeph"> h:mm:s，則同一時間顯示為1:07:5</span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-f42369774e2740dcb399626a0e4e930e}

選填。

## 預設 {#section-d016470e92a74f98a18c4ab3489410a5}

`m:ss`

## 範例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
chaptertimepattern=h:mm:ss
```

