---
title: SmartCropVideoPlayer.preload
description: 指出檢視器是否在播放開始之前開始載入視訊內容。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 7a83a02e-7b75-4f15-b8c1-aa7b64e6d3bd
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 2%

---

# SmartCropVideoPlayer.preload{#smartcropvideoplayer-preload}

指出檢視器是否在播放開始之前開始載入視訊內容。

`[SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer.]preload=0|1`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> 如果設為<span class="codeph"> 1 </span>，視訊會在資產設定後立即開始下載；否則，預先載入只會在一般使用者或API呼叫起始播放後開始。 </p> <p>若設為<span class="codeph"> 0 </span>，某些功能可能要在播放再次開始後才能運作；具體而言，搜尋作業不會更新視訊影格。 如果停用海報影像，檢視器會顯示為空白區域，而非第一個視訊影格。 </p> <p>在某些版本的Internet Explorer 11和Edge瀏覽器上，可能會忽略停用視訊預先載入。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

選擇性.

## 預設 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1`

## 範例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preload=0`
