---
description: VideoScrubber.timepattern
solution: Experience Manager
title: VideoScrubber.timepattern
feature: Dynamic Media Classic，檢視器，SDK/API，混合媒體集
role: Developer,Business Practitioner
exl-id: 0536110e-a885-4fd4-baa8-742fcdba5cc9
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 3%

---

# VideoScrubber.timepattern{#videoscrubber-timepattern}

`[VideoScrubber.|<containerId>_videoScrubber.]timepattern=[h:]m|mm:s|ss`

<table id="table_D1D7BE09311B469983B52E34338FEAFE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> 設定時間泡泡中顯示的時間模式，其中<span class="codeph"> h</span>為小時，<span class="codeph"> m</span>為分鐘，而<span class="codeph"> s</span>為秒。 </p> <p>每個時間單位使用的字母數決定單位要顯示的位數。 如果數字不能滿足給定位數，則等效值將以後續單位顯示。 </p> <p>例如，如果目前的影片時間是67分鐘5秒，則時間模式<span class="codeph"> m:ss</span>顯示為67:05。 如果給定的時間模式為<span class="codeph"> h:mm:s</span>，則將該時間顯示為1:07:5。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

選填。

## 預設 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`m:ss`

## 範例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`timepattern=h:mm:ss`
