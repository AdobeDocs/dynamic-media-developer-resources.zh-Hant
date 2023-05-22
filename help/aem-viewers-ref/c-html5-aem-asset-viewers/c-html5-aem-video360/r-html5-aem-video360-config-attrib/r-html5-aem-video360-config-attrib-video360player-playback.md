---
title: Video360Player.playback
description: Video360查看器的配置屬性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: e5a56195-c3ca-4748-aef6-e1f143ac254d
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 5%

---

# Video360Player.playback{#video-player-playback}

Video360查看器的配置屬性。

`[Video360Player.|<containerId>_video360Player.]playback=auto|progressive`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 自動累進</span> </p> </td> 
   <td colname="col2"> <p> 設定查看器使用的回放類型。 </p> <p>當 <span class="codeph"> 自動</span> 在大多數案頭瀏覽器和所有iOS設備中，查看器使用HLS格式的HTML5流視頻。 此外，它還可歸結於某些系統上的漸進式HTML5回放，如舊版Internet Explorer和Android™。 </p> <p>當 <span class="codeph"> 進步</span> 設定後，查看器僅依賴瀏覽器本機支援的HTML5播放，並在所有系統上逐步播放視頻。 </p> <p>有關中播放選擇的詳細資訊 <span class="codeph"> 自動</span> 和 <span class="codeph"> 進步</span> 本機模式，請參閱《HTML5查看器SDK使用手冊》。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

選擇性. 查看器處理外部視頻時忽略。

請參閱 [外部視頻支援](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-external-video-support.md#concept-66aa2784f2294794989bad2af74c3760) 的雙曲餘切值。

## 預設 {#section-71fb773f814649b2885aefee68073641}

`auto`

## 範例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`playback=progressive`
