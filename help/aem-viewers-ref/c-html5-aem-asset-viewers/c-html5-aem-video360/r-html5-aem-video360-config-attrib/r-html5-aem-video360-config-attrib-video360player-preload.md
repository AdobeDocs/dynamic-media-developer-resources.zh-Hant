---
title: Video360Player.preload
description: 指示查看器是否在播放開始之前開始載入視頻內容。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 33c28ed3-cdb3-4b14-8cc7-90f77ec9a3bb
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 6%

---

# Video360Player.preload{#video-player-preload}

指示查看器是否在播放開始之前開始載入視頻內容。

`[Video360Player.|<containerId>_video360Player.]preload=0|1`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> 如果設定為 <span class="codeph"> 1 </span>，在設定資產後立即開始下載視頻。 否則，只有在最終用戶或API調用啟動回放後才開始預載入。 </p> <p>如果設定為 <span class="codeph"> 0 </span>，某些功能在播放開始前可能無法正常工作。 具體來說，查找操作不更新視頻幀。 如果海報影像被禁用，則查看器將顯示為空區域，而不是第一個視頻幀。 </p> <p>在某些版本的Internet Explorer 11和Edge瀏覽器上，可忽略禁用視頻預載入。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

選擇性.

## 預設 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1`

## 範例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preload=0`
