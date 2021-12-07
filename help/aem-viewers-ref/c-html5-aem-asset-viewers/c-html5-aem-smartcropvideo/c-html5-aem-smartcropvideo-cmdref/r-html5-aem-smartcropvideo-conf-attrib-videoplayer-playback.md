---
title: SmartCropVideoPlayer.playback
description: 智慧型裁切視訊檢視器的設定屬性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
source-git-commit: dfd80e5727a128f272855f1f28e1bc89cb2436bf
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 2%

---

# SmartCropVideoPlayer.playback{#smartcropvideoplayer-playback}

智慧型裁切視訊檢視器的設定屬性。

`[SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer.]playback=auto|progressive`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 自動 — 漸進</span> </p> </td> 
   <td colname="col2"> <p> 設定檢視器使用的播放類型。 當 <span class="codeph"> 自動</span> 在大部分的案頭瀏覽器和所有iOS裝置上，檢視器都會使用HLS格式的HTML5串流視訊。 這可回復至某些系統上的漸進式HTML5播放，例如舊版Internet Explorer和Android™。 </p> <p>若 <span class="codeph"> 漸進式</span> 已指定，檢視器僅依賴瀏覽器原本支援的HTML5播放，並在所有系統上逐步播放視訊。 </p> <p>如需自動和漸進模式中播放選擇的詳細資訊，請參閱檢視器SDK使用指南。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-f42369774e2740dcb399626a0e4e930e}

選填。

檢視器與外部視訊搭配運作時忽略。 請參閱 [外部視訊支援]
(../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-external-video-support.md#concept-22c67fee43274a29b28ee16770b1b1f3)。

## 預設 {#section-d016470e92a74f98a18c4ab3489410a5}

`auto`

## 範例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
playback=progressive
```
