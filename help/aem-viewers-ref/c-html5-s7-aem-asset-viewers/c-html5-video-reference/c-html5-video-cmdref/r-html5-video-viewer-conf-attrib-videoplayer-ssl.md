---
description: 視訊檢視器的設定屬性。
solution: Experience Manager
title: VideoPlayer.ssl
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 2%

---


# VideoPlayer.ssl{#videoplayer-ssl}

視訊檢視器的設定屬性。

>[!NOTE]
>
>此配置屬性僅適用於安裝[功能包NPR-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480)的AEM6.2和安裝[功能包NPR-15011&lt;a3/AEM>的6.1。](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011)

`[VideoPlayer.|<containerId>_videoPlayer.]ssl=auto|on`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|on</span> </p> </td> 
   <td colname="col2"> <p> 控制視訊是透過安全SSL連線(HTTPS)還是不安全的連線(HTTP)傳送。 </p> <p>當設為<span class="codeph"> auto</span>時，視頻傳送協定繼承自嵌入網頁的協定。 如果網頁是透過HTTPS載入，視訊也會透過HTTPS傳送，反之亦然。 如果網頁位於HTTP上，則視訊會透過HTTP傳送。 </p> <p>當設為<span class="codeph"> on</span>時，視訊傳送一律會在安全連線上進行，而不考慮網頁通訊協定。 </p> <p>僅影響已發佈的視訊傳送，在「作者」模式中預覽視訊時會忽略。 </p> </td> 
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

另請參閱[安全視訊傳送](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-securevideodelivery.md#concept-cf9d1346a07d4429b0c6c32c9cac50ff)。
