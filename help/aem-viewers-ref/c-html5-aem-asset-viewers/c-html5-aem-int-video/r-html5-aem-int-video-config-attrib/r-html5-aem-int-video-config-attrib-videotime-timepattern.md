---
title: VideoTime.timepattern
description: Interactive Video Viewer的配置屬性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: de071adf-6c3c-4702-8950-8246b8ee459e
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 2%

---

# VideoTime.timepattern{#videotime-timepattern}

Interactive Video Viewer的配置屬性。

`[VideoTime.|<containerId>_videoTime.]timepattern=[h:]m|mm:s|ss`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> 設定在控制欄中顯示的時間的模式，其中 <span class="codeph"> h</span> 表示小時， <span class="codeph"> 米</span> 幾分鐘，然後 <span class="codeph"> s</span> 幾秒鐘。 </p> <p>每個時間單位使用的字母數決定單位顯示的位數。 如果數字不能容納給定數字，則在後續單位中顯示等效值。 </p> <p>例如，如果當前電影時間為67分5秒，則時間模式為 <span class="codeph"> m:ss</span> 顯示為67:05。 同時顯示為1:07:5如果時間模式為 <span class="codeph"> h:mm:s</span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

選擇性.

## 預設 {#section-71fb773f814649b2885aefee68073641}

`m:ss`

## 範例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
timepattern=h:mm:ss
```
