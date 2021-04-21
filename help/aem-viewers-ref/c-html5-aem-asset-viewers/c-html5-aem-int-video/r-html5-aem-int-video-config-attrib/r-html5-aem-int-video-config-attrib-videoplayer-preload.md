---
description: 指出檢視器是否在播放開始前開始載入視訊內容。
solution: Experience Manager
title: VideoPlayer.preload
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,Business Practitioner
exl-id: afabbfde-e003-4fee-a4ef-0fc4c43fd960
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 3%

---

# VideoPlayer.preload{#videoplayer-preload}

指出檢視器是否在播放開始前開始載入視訊內容。

`[VideoPlayer.|<containerId>_videoPlayer.]preload=0|1`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> 如果設為<span class="codeph"> 1 </span>，則視訊會在資產設定後立即開始下載；否則，預先載入只會在使用者或API呼叫開始播放後開始。 </p> <p>如果設定為<span class="codeph"> 0 </span>，則某些功能在播放開始之前可能無法工作；具體而言，搜尋操作不會更新視訊影格。 如果海報影像已停用，檢視器會以空白區域顯示，而非第一個視訊影格。 </p> <p>請注意，在某些版本的Internet Explorer 11和Edge瀏覽器上，停用視訊預先載入可能會被忽略。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

選填。

## 預設 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1`

## 範例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preload=0`
