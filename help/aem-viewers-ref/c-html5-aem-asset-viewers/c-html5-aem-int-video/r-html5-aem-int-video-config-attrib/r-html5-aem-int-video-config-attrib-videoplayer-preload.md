---
title: VideoPlayer.preload
description: 指出檢視器是否在播放開始之前開始載入視訊內容。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: afabbfde-e003-4fee-a4ef-0fc4c43fd960
TQID: 'https://experienceleague.adobe.com/T-tJLZX4XCIAQ6NjwNVYrbuM1czp25M6vAB0WVOZ1No'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 120
ht-degree: 4%

---

# VideoPlayer.preload{#videoplayer-preload}

指出檢視器是否在播放開始之前開始載入視訊內容。

`[VideoPlayer.|<containerId>_videoPlayer.]preload=0|1`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> 如果設為<span class="codeph"> 1 </span>，視訊會在資產設定後立即開始下載；否則，預先載入只會在一般使用者或API呼叫起始播放後開始。 </p> <p>如果設為<span class="codeph"> 0 </span>，某些功能在播放開始之前可能無法運作；具體而言，搜尋作業不會更新視訊影格。 如果停用海報影像，檢視器會顯示為空白區域，而非第一個視訊影格。 </p> <p>在某些版本的Internet Explorer 11和Edge瀏覽器上，可能會忽略停用視訊預先載入。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

選擇性.

## 預設 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1`

## 範例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preload=0`
