---
description: 互動式視訊檢視器的設定屬性。
seo-description: 互動式視訊檢視器的設定屬性。
seo-title: VideoPlayer.playback
solution: Experience Manager
title: VideoPlayer.playback
topic: Dynamic media
uuid: 2576f433-b9c2-4da1-9a51-f66b71d5df99
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7

---


# VideoPlayer.playback{#videoplayer-playback}

互動式視訊檢視器的設定屬性。

`[VideoPlayer.|<containerId>_videoPlayer.]playback=auto|progressive`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 自動——漸進</span> </p> </td> 
   <td colname="col2"> <p> 設定檢視器使用的播放類型。 </p> <p>設 <span class="codeph"> 定自動</span> 時，在大部分的案頭瀏覽器和所有iOS裝置中，檢視器會使用HLS格式的HTML5串流視訊，並回到某些系統（例如舊版Internet Explorer和Android）上漸進式HTML5播放。 </p> <p>設定漸 <span class="codeph"> 進式</span> 時，檢視器只會依賴HTML5播放（瀏覽器支援），並漸進式在所有系統上播放視訊。 </p> <p>如需自動和漸進式原生模式中播放選 <span class="codeph"> 擇的詳細資</span> 訊 <span class="codeph"></span> ，請參閱「HTML5檢視器SDK使用指南」。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

選填。

## 預設 {#section-71fb773f814649b2885aefee68073641}

`auto`

## 範例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`playback=progressive`
