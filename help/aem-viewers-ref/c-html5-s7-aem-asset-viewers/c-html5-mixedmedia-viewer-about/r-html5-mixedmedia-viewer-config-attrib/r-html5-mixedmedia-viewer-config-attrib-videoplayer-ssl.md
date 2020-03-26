---
description: 混合媒體視訊檢視器的設定屬性。
seo-description: 混合媒體視訊檢視器的設定屬性。
seo-title: VideoPlayer.ssl
solution: Experience Manager
title: VideoPlayer.ssl
topic: Dynamic media
uuid: 07e2c55b-2388-44c8-83ab-338997c5cb71
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# VideoPlayer.ssl{#videoplayer-ssl}

混合媒體視訊檢視器的設定屬性。

>[!NOTE]
>
>此設定屬性僅適用於安裝 [Feature Pack NPR-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) 的AEM 6.2和安裝 [Feature Pack NPR-15011的AEM 6.1](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011)。

`[VideoPlayer.|<containerId>_videoPlayer.]ssl=auto|on`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|on</span> </p> </td> 
   <td colname="col2"> <p> 控制視訊是透過安全SSL連線(HTTPS)還是不安全的連線(HTTP)傳送。 </p> <p>當設為自動 <span class="codeph"> 時</span> ，會從內嵌網頁的通訊協定繼承視訊傳送通訊協定。 如果網頁是透過HTTPS載入，視訊也會透過HTTPS傳送，反之亦然。 如果網頁位於HTTP上，則視訊會透過HTTP傳送。 </p> <p>設為on時 <span class="codeph"></span>，視訊傳送一律會在安全連線上進行，而不考慮網頁通訊協定。 </p> <p>僅影響已發佈的視訊傳送，在「作者」模式中預覽視訊時會忽略。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-f42369774e2740dcb399626a0e4e930e}

選填。

## 預設 {#section-d016470e92a74f98a18c4ab3489410a5}

`auto`

## 範例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
ssl=on
```

<!--<a id="section_5943AC73316749C68761FF7F74DA7547"></a>-->

另請參閱「 [保全視訊傳送」](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-securevideodelivery.md#concept-4d155111df9f469aa6c6d7b41e959dcb)。
