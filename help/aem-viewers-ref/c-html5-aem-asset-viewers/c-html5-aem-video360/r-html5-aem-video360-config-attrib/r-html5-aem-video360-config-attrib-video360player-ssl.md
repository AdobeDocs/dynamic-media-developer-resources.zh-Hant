---
title: Video360Player.ssl
description: Video360 Viewer的設定屬性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 44efa378-c911-4449-8a10-61212d4392c6
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 2%

---

# Video360Player.ssl{#video-player-ssl}

Video360 Viewer的設定屬性。

<!-- >[!NOTE]
>
>This configuration attribute only applies to AEM 6.2 with installation of [Feature Pack NPR-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) and to AEM 6.1 with installation of [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011). -->

`[Video360Player.|<containerId>_video360Player.]ssl=auto|on`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">自動|於</span> </p> </td> 
   <td colname="col2"> <p> 控制視訊是透過安全SSL連線(HTTPS)或不安全連線(HTTP)傳遞。 </p> <p>設定為<span class="codeph"> auto</span>時，視訊傳遞通訊協定繼承自內嵌網頁的通訊協定。 如果網頁是透過HTTPS載入，視訊也會透過HTTPS傳送，反之亦然。 如果網頁位於HTTP上，則會透過HTTP傳送影片。 </p> <p>在<span class="codeph">上設定為</span>時，無論網頁通訊協定為何，視訊傳送一律會透過安全連線進行。 </p> <p>只會影響已發佈的視訊傳送，且在「作者」模式中預覽視訊時會被忽略。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-f42369774e2740dcb399626a0e4e930e}

選擇性.

## 預設 {#section-d016470e92a74f98a18c4ab3489410a5}

`auto`

## 範例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
ssl=on
```

<!--<a id="section_5943AC73316749C68761FF7F74DA7547"></a>-->

另請參閱[安全視訊傳送](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-securevideodelivery.md#concept-13f66fdd4a52494aa516cd0f36fdac27)。
