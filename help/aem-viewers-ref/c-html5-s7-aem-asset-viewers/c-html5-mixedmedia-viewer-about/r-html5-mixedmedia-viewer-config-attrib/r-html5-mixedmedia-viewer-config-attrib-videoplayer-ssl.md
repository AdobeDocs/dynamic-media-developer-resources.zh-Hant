---
description: 混合媒體視訊檢視器的設定屬性。
solution: Experience Manager
title: VideoPlayer.ssl
feature: Dynamic Media Classic，檢視器，SDK/API，混合媒體集
role: Developer,Business Practitioner
exl-id: 5fd3aa39-edb0-4434-aa5f-e511c84cf950
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 2%

---

# VideoPlayer.ssl{#videoplayer-ssl}

混合媒體視訊檢視器的設定屬性。

>[!NOTE]
>
>此設定屬性僅適用於安裝[Feature Pack NPR-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480)的AEM 6.2，以及安裝[Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011)的AEM 6.1。

`[VideoPlayer.|<containerId>_videoPlayer.]ssl=auto|on`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 自動開啟</span> </p> </td> 
   <td colname="col2"> <p> 控制視訊是透過安全SSL連線(HTTPS)或不安全連線(HTTP)傳送。 </p> <p>設為<span class="codeph"> auto</span>時，視訊傳送通訊協定繼承自內嵌網頁的通訊協定。 如果網頁透過HTTPS載入，視訊也會透過HTTPS傳送，反之亦然。 如果網頁位於HTTP，則會透過HTTP傳送視訊。 </p> <p>當在</span>上設為<span class="codeph">時，視訊傳送一律會透過安全連線進行，而不考慮網頁通訊協定。 </span></p> <p>僅影響已發佈的視訊傳送，且會在「製作」模式中忽略視訊預覽。 </p> </td> 
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

另請參閱[安全視訊傳送](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-securevideodelivery.md#concept-4d155111df9f469aa6c6d7b41e959dcb)。
