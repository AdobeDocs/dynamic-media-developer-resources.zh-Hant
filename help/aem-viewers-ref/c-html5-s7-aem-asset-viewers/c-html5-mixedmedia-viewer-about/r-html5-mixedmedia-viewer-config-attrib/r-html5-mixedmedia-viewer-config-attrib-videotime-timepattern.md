---
title: VideoTime.timepattern
description: VideoTime.timepattern
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 0c79b3e2-ac5a-43c3-ac52-8240e7ed3cc1
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 3%

---

# VideoTime.timepattern{#videotime-timepattern}

`[VideoTime.|<containerId>_videoTime.]timepattern=[h:]m|mm:s|ss`

<table id="table_9FC55144166F406DB07DFE0C57791475"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> 設定在控制欄中顯示的時間的模式，其中 <span class="codeph"> h</span> 是小時， <span class="codeph"> 米</span> 是分鐘 <span class="codeph"> s</span> 秒。 </p> <p>每個時間單位使用的字母數決定單位顯示的位數。 如果數字不能容納給定數字，則在後續單位中顯示等效值。 </p> <p>例如，如果當前電影時間是67分5秒，則時間模式 <span class="codeph"> m:ss</span> 顯示為67:05。 同時顯示為1:07:5如果給定的時間模式 <span class="codeph"> h:mm:s</span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

選填。

## 預設 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`m:ss`

## 範例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`timepattern=h:mm:ss`
