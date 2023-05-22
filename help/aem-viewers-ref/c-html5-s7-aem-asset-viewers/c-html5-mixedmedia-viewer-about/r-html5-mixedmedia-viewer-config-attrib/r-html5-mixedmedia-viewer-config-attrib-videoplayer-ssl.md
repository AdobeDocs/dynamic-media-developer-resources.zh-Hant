---
title: VideoPlayer.ssl
description: 混合媒體視頻查看器的配置屬性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 5fd3aa39-edb0-4434-aa5f-e511c84cf950
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 2%

---

# VideoPlayer.ssl{#videoplayer-ssl}

混合媒體視頻查看器的配置屬性。

<!-- >[!NOTE]
>
>This configuration attribute only applies to AEM 6.2 with installation of [Feature Pack NPR-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) and to AEM 6.1 with installation of [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011). -->

`[VideoPlayer.|<containerId>_videoPlayer.]ssl=auto|on`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 自動|開啟</span> </p> </td> 
   <td colname="col2"> <p> 控制視頻是通過安全SSL連接(HTTPS)還是不安全連接(HTTP)傳送的。 </p> <p>設定為時 <span class="codeph"> 自動</span> 視頻傳送協定從嵌入網頁的協定中繼承。 如果網頁是通過HTTPS載入的，則視頻也是通過HTTPS傳送的，反之也是通過HTTPS傳送的。 如果網頁在HTTP上，則通過HTTP傳送視頻。 </p> <p>設定為時 <span class="codeph"> 上</span>，視頻傳輸始終通過安全連接進行，而不考慮網頁協定。 </p> <p>僅影響已發佈的視頻傳送，在「作者」模式下，將忽略視頻預覽。 </p> </td> 
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

另請參閱 [安全視頻傳送](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-securevideodelivery.md#concept-4d155111df9f469aa6c6d7b41e959dcb)。
