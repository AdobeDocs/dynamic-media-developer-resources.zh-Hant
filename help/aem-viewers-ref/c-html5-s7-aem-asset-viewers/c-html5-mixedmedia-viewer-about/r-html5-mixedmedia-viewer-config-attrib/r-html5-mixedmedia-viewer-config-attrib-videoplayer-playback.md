---
description: 混合媒體視訊檢視器的設定屬性。
solution: Experience Manager
title: VideoPlayer.playback
feature: Dynamic Media Classic，檢視器，SDK/API，混合媒體集
role: Developer,Business Practitioner
exl-id: accf2b56-d7bd-483d-9759-fa38246a0a8f
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 3%

---

# VideoPlayer.playback{#videoplayer-playback}

混合媒體視訊檢視器的設定屬性。

`[VideoPlayer.|<containerId>_videoPlayer.]playback=auto|progressive`

<table id="table_27B4B2DDD44D4D1CB46DD1906A92B2FD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 自動 — 漸進</span> </p> </td> 
   <td colname="col2"> <p> 設定檢視器使用的播放類型。 當設定<span class="codeph"> auto</span>時，在大部分的案頭瀏覽器和所有iOS裝置上，檢視器會使用HLS格式的HTML5串流視訊。 這會回復至某些系統（例如舊版Internet Explorer和Android）上的漸進式HTML5播放。 </p> <p>如果指定<span class="codeph">漸進式</span>，則檢視器僅依賴HTML5播放，如同瀏覽器原本支援的一樣，並在所有系統上逐步播放視訊。 </p> <p>如需自動和漸進模式中播放選擇的詳細資訊，請參閱檢視器SDK使用指南。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

選填。

## 預設 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`auto`

## 範例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`playback=progressive`
