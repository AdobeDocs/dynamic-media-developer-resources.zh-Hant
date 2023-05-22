---
title: VideoPlayer.playback
description: Interactive Video Viewer的配置屬性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: fa49e025-1a46-4be7-ad1e-eda3b31bdc8d
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 2%

---

# VideoPlayer.playback{#videoplayer-playback}

Interactive Video Viewer的配置屬性。

`[VideoPlayer.|<containerId>_videoPlayer.]playback=auto|progressive`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 自動累進</span> </p> </td> 
   <td colname="col2"> <p> 設定查看器使用的回放類型。 </p> <p>當 <span class="codeph"> 自動</span> 在大多數案頭瀏覽器和所有iOS設備中，查看器使用HLS格式的HTML5流視頻。 此外，它還可歸結於某些系統上的漸進式HTML5回放，如舊版Internet Explorer和Android™。 </p> <p>當 <span class="codeph"> 進步</span> 設定後，查看器僅依賴瀏覽器本機支援的HTML5播放，並在所有系統上逐步播放視頻。 </p> <p>有關中播放選擇的詳細資訊 <span class="codeph"> 自動</span> 和 <span class="codeph"> 進步</span> 本機模式，請參閱《HTML5查看器SDK使用手冊》。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

選擇性.

## 預設 {#section-71fb773f814649b2885aefee68073641}

`auto`

## 範例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`playback=progressive`
