---
description: Video360檢視器的設定屬性。
seo-description: Video360檢視器的設定屬性。
seo-title: Video360Player.playback
solution: Experience Manager
title: Video360Player.playback
topic: Dynamic media
uuid: ce814963-5cb8-408e-9d57-e7b7e61e0fab
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Video360Player.playback{#video-player-playback}

Video360檢視器的設定屬性。

`[Video360Player.|<containerId>_video360Player.]playback=auto|progressive`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 自動——漸進</span> </p> </td> 
   <td colname="col2"> <p> 設定檢視器使用的播放類型。 </p> <p>設 <span class="codeph"> 定自動</span> 時，在大部分的案頭瀏覽器和所有iOS裝置中，檢視器會使用HLS格式的HTML5串流視訊，並回到某些系統（例如舊版Internet Explorer和Android）上漸進式HTML5播放。 </p> <p>設定漸 <span class="codeph"> 進式</span> 時，檢視器只會依賴HTML5播放（瀏覽器支援），並漸進式在所有系統上播放視訊。 </p> <p>如需自動和漸進式原生模式中播放選 <span class="codeph"> 擇的詳細資</span> 訊 <span class="codeph"></span> ，請參閱「HTML5檢視器SDK使用指南」。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

選填。當檢視器與外部視訊搭配運作時已忽略。

如需詳 [細資訊，請參閱外部](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-external-video-support.md#concept-66aa2784f2294794989bad2af74c3760) 視訊支援。

## 預設 {#section-71fb773f814649b2885aefee68073641}

`auto`

## 範例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`playback=progressive`
