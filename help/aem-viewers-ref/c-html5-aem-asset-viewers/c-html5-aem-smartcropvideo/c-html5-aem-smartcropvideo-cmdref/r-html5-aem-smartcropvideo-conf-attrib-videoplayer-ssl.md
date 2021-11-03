---
description: 智慧型裁切視訊檢視器的設定屬性。
solution: Experience Manager
title: SmartCropVideoPlayer.ssl
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: f7d832f3-e9b1-4161-a572-851e538bb245
source-git-commit: bdef251dcbb7c135d02813e9fd82e2e5e32300cc
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 3%

---

# SmartCropVideoPlayer.ssl{#smartcropvideoplayer-ssl}

智慧型裁切視訊檢視器的設定屬性。

<!-- >[!NOTE]
>
>This configuration attribute only applies to AEM 6.2 with installation of [Feature Pack NPR-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) and to AEM 6.1 with installation of [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011). -->

`[SmartCropVideoPlayer.|<containerId>_videoPlayer.]ssl=auto|on`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 自動開啟</span> </p> </td> 
   <td colname="col2"> <p> 控制視訊是透過安全SSL連線(HTTPS)或不安全連線(HTTP)傳送。 </p> <p>設為時 <span class="codeph"> 自動</span> 視訊傳送通訊協定繼承自內嵌網頁的通訊協定。 如果網頁透過HTTPS載入，視訊也會透過HTTPS傳送，反之亦然。 如果網頁位於HTTP，則會透過HTTP傳送視訊。 </p> <p>設為時 <span class="codeph"> on</span>，視訊傳送一律會透過安全連線進行，而不考慮網頁通訊協定。 </p> <p>僅影響已發佈的視訊傳送，且會在「製作」模式中忽略視訊預覽。 </p> </td> 
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

另請參閱 [安全視訊傳送](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-securevideodelivery.md#concept-cf9d1346a07d4429b0c6c32c9cac50ff).
