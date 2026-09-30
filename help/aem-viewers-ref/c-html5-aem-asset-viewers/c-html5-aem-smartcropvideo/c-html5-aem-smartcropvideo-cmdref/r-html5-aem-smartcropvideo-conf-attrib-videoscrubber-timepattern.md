---
title: VideoScrubber.timepattern
description: 智慧型裁切視訊檢視器的設定屬性。
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 4b3082f6-fb88-4c69-ab09-e24cff039222
TQID: 'https://experienceleague.adobe.com/sf1HQhhJ5AMww71mc2zZhZK2HQlr-XeI9QBBK4ZnBRo'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
  - id: d09181b5-a36a-43de-ba01-36641440bc43
    internal-label: Experience Manager Assets
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
    internal-label: APIs
  - id: fe490c45-63fa-5b99-b5b4-d8cfeda8aa7d
    internal-label: SDK/API
  - id: bd0d2470-932c-4269-8eca-6d939b72d9ef
    internal-label: Dynamic Media
  - id: d4b6216b-4a89-4ff0-8ac0-5a699ba23100
    internal-label: Images and videos
subfeature_v2:
  - id: c12bda38-aa1a-4647-b62e-42cd4537dac6
    internal-label: Dynamic Media Classic
  - id: d17d085a-e808-49dd-b9a6-85a996b999bd
    internal-label: Viewers
  - id: a0cde32c-c339-4649-bd06-f1111bc952fc
    internal-label: Smart Crop
  - id: cb04d42d-1b70-43b0-9951-45998eb6e842
    internal-label: Video
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: 0e24e07f8c91d3e7fda5510ed4252f9953e27467
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 2%
---
# VideoScrubber.timepattern{#videoscrubber-timepattern}

智慧型裁切視訊檢視器的設定屬性。

`[VideoScrubber.|<containerId>_videoScrubber.]timepattern=[h:]m|mm:s|ss`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h：]m|mm：s|ss</span> </p> </td> 
   <td colname="col2"> <p> 設定時間泡泡中顯示的時間模式，其中<span class="codeph"> h</span>是小時，<span class="codeph"> m</span>是分鐘，而<span class="codeph"> s</span>是秒。 </p> <p>用於每個時間單位的字母數目決定該單位要顯示的位數。 如果數字不符合指定的位數，則會在後續單位中顯示對等值。 </p> <p>例如，如果目前的影片時間為67分5秒，則時間模式<span class="codeph"> m：ss</span>會顯示為67:05。 如果指定的時間模式為<span class="codeph"> h:mm:s</span>，則相同的時間會顯示為1:07:5。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-f42369774e2740dcb399626a0e4e930e}

選擇性.

## 預設 {#section-d016470e92a74f98a18c4ab3489410a5}

`m:ss`

## 範例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
timepattern=h:mm:ss
```
