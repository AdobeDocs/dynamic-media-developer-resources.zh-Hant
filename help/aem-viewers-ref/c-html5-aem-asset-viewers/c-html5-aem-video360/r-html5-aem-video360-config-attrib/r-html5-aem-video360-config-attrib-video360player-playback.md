---
title: Video360Player.playback
description: Video360 Viewer的設定屬性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: e5a56195-c3ca-4748-aef6-e1f143ac254d
TQID: 'https://experienceleague.adobe.com/2Q41XrgRhpCJXlpHtdIVJkcy2eqVNTK4lSo023yPRoI'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 122
ht-degree: 2%

---

# Video360Player.playback{#video-player-playback}

Video360 Viewer的設定屬性。

`[Video360Player.|<containerId>_video360Player.]playback=auto|progressive`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">自動|漸進式</span> </p> </td> 
   <td colname="col2"> <p> 設定檢視器使用的播放型別。 </p> <p>設定<span class="codeph"> auto</span>時，在大部分的案頭瀏覽器和所有iOS裝置上，檢視器會使用HLS格式的HTML5串流視訊。 此外，它也會退回某些系統（例如舊版Internet Explorer和™）上的漸進式HTML5播放。 </p> <p>設定<span class="codeph"> progressive</span>時，檢視器僅依賴瀏覽器原生支援的HTML5播放，並在所有系統上以漸進方式播放視訊。 </p> <p>如需有關<span class="codeph">自動</span>和<span class="codeph">漸進式</span>原生模式中播放選擇的詳細資訊，請參閱HTML5 Viewers SDK使用手冊。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

選擇性. 當檢視器搭配外部視訊使用時忽略。

如需詳細資訊，請參閱[外部視訊支援](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-external-video-support.md#concept-66aa2784f2294794989bad2af74c3760)。

## 預設 {#section-71fb773f814649b2885aefee68073641}

`auto`

## 範例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`playback=progressive`
