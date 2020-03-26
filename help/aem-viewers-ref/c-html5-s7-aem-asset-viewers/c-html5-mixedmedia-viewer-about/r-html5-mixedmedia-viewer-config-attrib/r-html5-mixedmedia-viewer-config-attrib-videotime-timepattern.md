---
description: 'null'
seo-description: 'null'
seo-title: VideoTime.timepattern
solution: Experience Manager
title: VideoTime.timepattern
topic: Dynamic media
uuid: 57c86b63-7495-4f6f-bd30-8c4ebf017e36
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# VideoTime.timepattern{#videotime-timepattern}

`[VideoTime.|<containerId>_videoTime.]timepattern=[h:]m|mm:s|ss`

<table id="table_9FC55144166F406DB07DFE0C57791475"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> 設定控制列中顯示的時間模式，其中 <span class="codeph"> h</span> 為小時、 <span class="codeph"> m</span> 為分鐘 <span class="codeph"> 和</span> s為秒。 </p> <p>每個時間單位使用的字母數決定單位要顯示的位數。 如果數字不能與給定數字匹配，則等效值將顯示在後續單位中。 </p> <p>例如，如果目前的影片時間是67分5秒，時間模式 <span class="codeph"> m:ss</span> 會顯示為67:05。 如果給定時間模式為 <span class="codeph"> h:mm:s，則同一時間顯示為1:07:5</span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

選填。

## 預設 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`m:ss`

## 範例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`timepattern=h:mm:ss`
