---
title: SmartCropVideoPlayer.playback
description: Smart Crop Video Viewer的配置屬性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 6df94fe7-30ea-42f1-a39e-50219259a098
source-git-commit: 8c49595fe0efb684b59601fb268bd8bf97fae555
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 2%

---

# SmartCropVideoPlayer.playback{#smartcropvideoplayer-playback}

Smart Crop Video Viewer的配置屬性。

`[SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer.]playback=auto|progressive`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 自動累進</span> </p> </td> 
   <td colname="col2"> <p> 設定查看器使用的回放類型。 當 <span class="codeph"> 自動</span> 在大多數案頭瀏覽器和所有iOS設備上，查看器使用HLS格式的HTML5流視頻。 它回歸到某些系統上的漸進式HTML5回放，如舊版Internet Explorer和Android™。 </p> <p>如果 <span class="codeph"> 進步</span> 指定後，查看器僅依賴瀏覽器本機支援的HTML5播放，並在所有系統上逐步播放視頻。 </p> <p>有關自動和漸進模式下播放選擇的詳細資訊，請參閱《Viewer SDK使用手冊》。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-f42369774e2740dcb399626a0e4e930e}

選擇性.

查看器處理外部視頻時忽略。 請參閱 [外部視頻支援]
(../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-external-video-support.md#concept-22c67fee43274a29b28ee16770b1b1f3)。

## 預設 {#section-d016470e92a74f98a18c4ab3489410a5}

`auto`

## 範例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
playback=progressive
```
