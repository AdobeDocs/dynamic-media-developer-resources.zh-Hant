---
title: SmartCropVideoPlayer.preload
description: 指出檢視器是否在播放開始前開始載入視訊內容。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
source-git-commit: 2dc7b92da6c73a328a82c50dc5a052a3351ee2dc
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 4%

---

# SmartCropVideoPlayer.preload{#smartcropvideoplayer-preload}

指出檢視器是否在播放開始前開始載入視訊內容。

`[SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer.]preload=0|1`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> 若設為 <span class="codeph"> 1 </span> 資產設定後，影片即會開始下載；否則，預先載入只會在使用者或API呼叫起始播放後開始。 </p> <p>若設為 <span class="codeph"> 0 </span> 某些功能要等到重新開始播放才能運作；具體而言，搜尋操作不會更新視訊幀。 如果海報影像已停用，檢視器會顯示為空白區域，而非第一個視訊影格。 </p> <p>某些版本的Internet Explorer 11和Edge瀏覽器可能會忽略停用視訊預先載入。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

選填。

## 預設 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1`

## 範例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preload=0`
