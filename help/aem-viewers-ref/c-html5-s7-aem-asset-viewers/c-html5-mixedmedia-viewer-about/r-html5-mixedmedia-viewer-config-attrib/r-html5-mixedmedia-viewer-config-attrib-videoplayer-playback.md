---
title: VideoPlayer.playback
description: 混合媒體視頻查看器的配置屬性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: accf2b56-d7bd-483d-9759-fa38246a0a8f
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 3%

---

# VideoPlayer.playback{#videoplayer-playback}

混合媒體視頻查看器的配置屬性。

`[VideoPlayer.|<containerId>_videoPlayer.]playback=auto|progressive`

<table id="table_27B4B2DDD44D4D1CB46DD1906A92B2FD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 自動累進</span> </p> </td> 
   <td colname="col2"> <p> 設定查看器使用的回放類型。 當 <span class="codeph"> 自動</span> 在大多數案頭瀏覽器和所有iOS設備上，查看器使用HLS格式的HTML5流視頻。 它回歸到某些系統上的漸進式HTML5回放，如舊版Internet Explorer和Android™。 </p> <p>如果 <span class="codeph"> 進步</span> 指定後，查看器僅依賴瀏覽器本機支援的HTML5播放，並在所有系統上逐步播放視頻。 </p> <p>有關自動和漸進模式下播放選擇的詳細資訊，請參閱《Viewer SDK使用手冊》。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

選填。

## 預設 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`auto`

## 範例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`playback=progressive`
