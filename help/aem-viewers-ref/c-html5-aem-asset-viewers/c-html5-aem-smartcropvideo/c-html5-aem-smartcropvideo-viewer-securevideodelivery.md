---
title: HTTP視訊傳送
description: HTTP視訊傳送
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: b809a11f-3c2d-4abd-b317-fabb36245b1b
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 0%

---

# HTTP視訊傳送{#http-video-delivery}

<!-- >[!NOTE]
>
>Secure Video Delivery only applies to AEM 6.2 with the installation of [Feature Pack-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) and to AEM 6.1 with installation of [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011). -->

如果檢視器在設定中運作（如本節開頭所述），已發佈的視訊傳送可能會在HTTPS （安全）和HTTP （不安全）模式中發生。 在預設設定中，視訊傳送通訊協定會嚴格遵循內嵌網頁的傳送通訊協定。 不過，即使使用[SmartCropVideoPlayer.ssl](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/r-html5-mixedmedia-viewer-config-attrib/r-html5-mixedmedia-viewer-config-attrib-videoplayer-ssl.md#reference-df0a29aa8a584cebaaa1c7bb6fab362e)設定屬性內嵌網頁所使用的通訊協定，也可以強制執行HTTPS視訊傳送。 （作者模式下的視訊預覽一律會透過HTTPS安全地傳送。）

根據您在Adobe Experience Manager中使用的Dynamic Media視訊發佈方法，`SmartCropVideoPlayer.ssl`設定屬性的套用方式會有所不同，如下列所示：

* 如果您使用URL發佈Dynamic Media視訊，則會將`SmartCropVideoPlayer.ssl`附加至URL。 例如，若要強制進行安全視訊傳送，您可以將`&SmartCropVideoPlayer.ssl=on`附加至下列檢視器URL範例的結尾：

  ```
  https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/SmartCropVideoViewer.html?asset=%2Fcontent%2Fdam%2Fmarketing%2Fshoppable-video%2Fadobe-axis-demo%2FAdobe_AXIS_V3_GRADED-HD.mp4&config=/etc/dam/presets/viewer/Video&serverUrl=https%3A%2F%2Fadobedemo62-h.assetsadobe.com%2Fis%2Fimage%2F&contenturl=%2F&config2=/etc/dam/presets/analytics&videoserverurl=https://gateway-na.assetsadobe.com/DMGateway/public/demoCo&posterimage=/content/dam/marketing/shoppable-video/adobe-axis-demo/Adobe_AXIS_V3_GRADED-HD.mp4&SmartCropVideoPlayer.ssl=on
  ```

  另請參閱[將URL連結至您的網頁應用程式](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html?lang=en#dynamic)。

* 如果您使用內嵌程式碼發佈Dynamic Media視訊，請將`SmartCropVideoPlayer.ssl`新增至內嵌程式碼片段中的其他檢視器組態引數清單。 例如，若要強制HTTPS視訊傳送，您可以附加`&SmartCropVideoPlayer.ssl=on`，如下列範例所示：

  ```
  <style type="text/css"> 
   #s7video_div.s7videoviewer{ 
     width:100%;  
     height:auto; 
   } 
  </style> 
  <script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/SmartCropVideoViewer.js"></script> 
  <div id="s7video_div"></div> 
  <script type="text/javascript"> 
   var s7videoviewer = new s7viewers.SmartCropVideoViewer({ 
    "containerId" : "s7video_div", 
    "params" : {  
     "SmartCropVideoPlayer.ssl" : "on", 
     "serverurl" : "https://adobedemo62-h.assetsadobe.com/is/image", 
     "contenturl" : "https://demos-pub.assetsadobe.com/",  
     "config" : "/etc/dam/presets/viewer/Video", 
     "config2": "/etc/dam/presets/analytics", 
     "videoserverurl": "https://gateway-na.assetsadobe.com/DMGateway/public/demoCo", 
     "posterimage": "/content/dam/marketing/shoppable-video/adobe-axis-demo/Adobe_AXIS_V3_GRADED-HD.mp4", 
     "asset" : "/content/dam/marketing/shoppable-video/adobe-axis-demo/Adobe_AXIS_V3_GRADED-HD.mp4" } 
   }).init(); 
  </script>
  ```

  另請參閱[在網頁上內嵌視訊](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html#dynamic)。
