---
title: VideoPlayer.preload
description: 指示查看器是否在播放開始之前開始載入視頻內容。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 90fb988a-255c-46fe-b05a-39c95ae8b95d
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 3%

---

# VideoPlayer.preload{#videoplayer-preload}

指示查看器是否在播放開始之前開始載入視頻內容。

`[VideoPlayer.|<containerId>_videoPlayer.]preload=0|1`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> 如果設定為 <span class="codeph"> 1 </span> 視頻在設定資產後立即開始下載；否則，只有在最終用戶或API調用啟動回放後才開始預載入。 </p> <p>如果設定為 <span class="codeph"> 0 </span> 某些功能在播放開始前可能無法工作；具體來說，搜索操作不更新視頻幀。 如果海報影像被禁用，則查看器將顯示為空區域，而不是第一個視頻幀。 </p> <p>在某些版本的Internet Explorer 11和Edge瀏覽器上，可忽略禁用視頻預載入。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

選擇性.

## 預設 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1`

## 範例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preload=0`
