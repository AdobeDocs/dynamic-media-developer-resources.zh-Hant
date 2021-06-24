---
description: 指出檢視器是否在播放開始前開始載入視訊內容。
solution: Experience Manager
title: Video360Player.preload
feature: Dynamic Media Classic，檢視器，SDK/API,360 VR影片
role: Developer,Business Practitioner
exl-id: 33c28ed3-cdb3-4b14-8cc7-90f77ec9a3bb
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 6%

---

# Video360Player.preload{#video-player-preload}

指出檢視器是否在播放開始前開始載入視訊內容。

`[Video360Player.|<containerId>_video360Player.]preload=0|1`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> 如果設為<span class="codeph"> 1 </span>，視訊會在資產設定後立即開始下載；否則，預先載入只會在使用者或API呼叫起始播放後開始。 </p> <p>如果設為<span class="codeph"> 0 </span> ，某些功能可能要等到播放開始時才能運作；具體而言，搜尋操作不會更新視訊幀。 如果海報影像已停用，檢視器會顯示為空白區域，而非第一個視訊影格。 </p> <p>請注意，某些版本的Internet Explorer 11和Edge瀏覽器可能會忽略停用視訊預先載入。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

選填。

## 預設 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1`

## 範例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preload=0`
