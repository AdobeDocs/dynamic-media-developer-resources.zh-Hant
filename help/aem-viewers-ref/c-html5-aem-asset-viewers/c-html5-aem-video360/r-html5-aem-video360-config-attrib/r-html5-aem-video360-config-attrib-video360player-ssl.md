---
description: Video360查看器的配置屬性。
solution: Experience Manager
title: Video360Player.ssl
feature: Dynamic Media Classic，檢視器，SDK/API,360 VR影片
role: Developer,Business Practitioner
exl-id: 44efa378-c911-4449-8a10-61212d4392c6
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 4%

---

# Video360Player.ssl{#video-player-ssl}

Video360查看器的配置屬性。

>[!NOTE]
>
>此設定屬性僅適用於安裝[Feature Pack NPR-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480)的AEM 6.2，以及安裝[Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011)的AEM 6.1。

`[Video360Player.|<containerId>_video360Player.]ssl=auto|on`

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

另請參閱[安全視訊傳送](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-securevideodelivery.md#concept-13f66fdd4a52494aa516cd0f36fdac27)。
