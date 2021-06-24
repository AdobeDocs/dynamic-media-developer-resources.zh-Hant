---
description: 視訊檢視器的設定屬性。
solution: Experience Manager
title: VideoPlayer.playback
feature: Dynamic Media Classic，檢視器， SDK/API，影片
role: Developer,Business Practitioner
exl-id: 54a10b30-ebf5-4f1e-aa4a-b09055453c4e
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 3%

---

# VideoPlayer.playback{#videoplayer-playback}

視訊檢視器的設定屬性。

`[VideoPlayer.|<containerId>_videoPlayer.]playback=auto|progressive`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 自動 — 漸進</span> </p> </td> 
   <td colname="col2"> <p> 設定檢視器使用的播放類型。 當設定<span class="codeph"> auto</span>時，在大部分的案頭瀏覽器和所有iOS裝置上，檢視器會使用HLS格式的HTML5串流視訊。 這會回復至某些系統（例如舊版Internet Explorer和Android）上的漸進式HTML5播放。 </p> <p>如果指定<span class="codeph">漸進式</span>，則檢視器僅依賴HTML5播放，如同瀏覽器原本支援的一樣，並在所有系統上逐步播放視訊。 </p> <p>如需自動和漸進模式中播放選擇的詳細資訊，請參閱檢視器SDK使用指南。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-f42369774e2740dcb399626a0e4e930e}

選填。

檢視器與外部視訊搭配運作時忽略。 請參閱[外部視訊支援](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-external-video-support.md#concept-22c67fee43274a29b28ee16770b1b1f3)。

## 預設 {#section-d016470e92a74f98a18c4ab3489410a5}

`auto`

## 範例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
playback=progressive
```
