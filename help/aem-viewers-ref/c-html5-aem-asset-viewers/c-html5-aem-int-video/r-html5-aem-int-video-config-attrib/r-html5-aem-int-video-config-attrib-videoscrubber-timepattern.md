---
title: VideoScrubber.timepattern
description: 互動式視訊檢視器的設定屬性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: d39ddf38-9157-412a-83a4-c1af4944a904
TQID: 'https://experienceleague.adobe.com/ZNw6n5Zokz-s696GvaLkQJY-fAT-JoNafyLzpztZqos'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 118
ht-degree: 2%

---

# VideoScrubber.timepattern{#videoscrubber-timepattern}

互動式視訊檢視器的設定屬性。

`[VideoScrubber.|<containerId>_videoScrubber.]timepattern=[h:]m|mm:s|ss`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h：]m|mm：s|ss</span> </p> </td> 
   <td colname="col2"> <p> 設定時間泡泡中顯示的時間模式，其中<span class="codeph"> h</span>代表小時、<span class="codeph"> m</span>代表分鐘、<span class="codeph"> s</span>代表秒。 </p> <p>用於每個時間單位的字母數目決定該單位要顯示的位數。 如果數字不符合指定的位數，則會在後續單位中顯示對等值。 </p> <p>例如，如果目前的影片時間為67分5秒，則時間模式<span class="codeph"> m：ss</span>會顯示為67:05。 如果時間模式為<span class="codeph"> h:mm:s</span>，則相同的時間會顯示為1:07:5。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

選擇性.

## 預設 {#section-71fb773f814649b2885aefee68073641}

`mm:s`

## 範例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
timepattern=h:mm:ss
```
