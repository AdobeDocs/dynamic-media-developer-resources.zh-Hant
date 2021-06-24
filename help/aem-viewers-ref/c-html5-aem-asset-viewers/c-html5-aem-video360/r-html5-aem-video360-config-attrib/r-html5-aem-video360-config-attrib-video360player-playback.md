---
description: Video360查看器的配置屬性。
solution: Experience Manager
title: Video360Player.playback
feature: Dynamic Media Classic，檢視器，SDK/API,360 VR影片
role: Developer,Business Practitioner
exl-id: e5a56195-c3ca-4748-aef6-e1f143ac254d
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 6%

---

# Video360Player.playback{#video-player-playback}

Video360查看器的配置屬性。

`[Video360Player.|<containerId>_video360Player.]playback=auto|progressive`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 自動 — 漸進</span> </p> </td> 
   <td colname="col2"> <p> 設定檢視器使用的播放類型。 </p> <p>當設定<span class="codeph"> auto</span>時，在大部分的案頭瀏覽器和所有iOS裝置中，檢視器會使用HLS格式的HTML5串流視訊，並回復為在某些系統（例如舊版Internet Explorer和Android）上漸進式HTML5播放。 </p> <p>當設定<span class="codeph">漸進式</span>時，檢視器僅依賴瀏覽器原本支援的HTML5播放，並在所有系統上逐步播放視訊。 </p> <p>如需<span class="codeph"> auto</span>和<span class="codeph">漸進式</span>原生模式中播放選取的詳細資訊，請參閱HTML5檢視器SDK使用手冊。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

選填。當檢視器與外部視訊搭配運作時忽略。

如需詳細資訊，請參閱[外部視訊支援](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-external-video-support.md#concept-66aa2784f2294794989bad2af74c3760) 。

## 預設 {#section-71fb773f814649b2885aefee68073641}

`auto`

## 範例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`playback=progressive`
