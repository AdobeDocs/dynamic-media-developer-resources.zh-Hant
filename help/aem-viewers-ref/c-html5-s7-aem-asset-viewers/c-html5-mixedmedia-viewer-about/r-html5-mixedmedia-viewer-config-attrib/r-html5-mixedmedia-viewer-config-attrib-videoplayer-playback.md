---
description: 混合媒體視訊檢視器的設定屬性。
seo-description: 混合媒體視訊檢視器的設定屬性。
seo-title: VideoPlayer.playback
solution: Experience Manager
title: VideoPlayer.playback
topic: Dynamic media
uuid: 7016d414-aa93-4854-8f95-24e94082b5ce
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# VideoPlayer.playback{#videoplayer-playback}

混合媒體視訊檢視器的設定屬性。

`[VideoPlayer.|<containerId>_videoPlayer.]playback=auto|progressive`

<table id="table_27B4B2DDD44D4D1CB46DD1906A92B2FD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 自動——漸進</span> </p> </td> 
   <td colname="col2"> <p> 設定檢視器使用的播放類型。 當設 <span class="codeph"> 定自動</span> (auto)時，在大部分的案頭瀏覽器和所有iOS裝置上，檢視器會使用HLS格式的HTML5串流視訊。 它可回溯至某些系統上的漸進式HTML5播放，例如舊版Internet Explorer和Android。 </p> <p>如果 <span class="codeph"> 指定漸進式</span> ，檢視器只會依賴HTML5播放（瀏覽器支援），並漸進式在所有系統上播放視訊。 </p> <p>如需自動和漸進式模式中播放選擇的詳細資訊，請參閱檢視器SDK使用指南。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

選填。

## 預設 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`auto`

## 範例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`playback=progressive`
