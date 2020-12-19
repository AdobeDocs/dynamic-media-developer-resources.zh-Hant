---
description: 'null'
seo-description: 'null'
seo-title: HTTP視訊傳送
solution: Experience Manager
title: HTTP視訊傳送
topic: Dynamic media
uuid: fd02a55a-a0f1-47a2-983f-15f296d1dbb4
translation-type: tm+mt
source-git-commit: 6cff4553307fe6cbda4b80ce3f39b58e615fa365
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 0%

---


# HTTP視訊傳送{#http-video-delivery}

>[!NOTE]
>
>「安全視訊傳送」僅適用於安裝[功能套件-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480)的AEM 6.2，以及安裝[功能套件NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011)的AEM 6.1。

如果檢視器如本節開頭所述的設定運作，發佈的視訊傳送可在HTTPS（安全）和HTTP（不安全）模式下進行。 在預設配置中，視訊傳送通訊協定會嚴格遵循內嵌網頁的傳送通訊協定。 不過，不論使用[VideoPlayer.ssl](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/r-html5-mixedmedia-viewer-config-attrib/r-html5-mixedmedia-viewer-config-attrib-videoplayer-ssl.md#reference-df0a29aa8a584cebaaa1c7bb6fab362e)組態屬性內嵌網頁所使用的通訊協定，都可強制HTTPS視訊傳送。 （請注意，在「作者」模式中的視訊預覽一律會透過HTTPS安全地傳送。）

根據您在AEM中使用的發佈動態媒體視訊方法，`VideoPlayer.ssl`組態屬性的套用方式與下列所示不同：

* 如果您使用URL發佈動態媒體影片，請將`VideoPlayer.ssl`附加至URL。 例如，若要強制安全傳送視訊，請將`&VideoPlayer.ssl=on`附加至下列檢視器URL範例的結尾：

   ```
   https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/VideoViewer.html?asset=%2Fcontent%2Fdam%2Fmarketing%2Fshoppable-video%2Fadobe-axis-demo%2FAdobe_AXIS_V3_GRADED-HD.mp4&config=/etc/dam/presets/viewer/Video&serverUrl=https%3A%2F%2Fadobedemo62-h.assetsadobe.com%2Fis%2Fimage%2F&contenturl=%2F&config2=/etc/dam/presets/analytics&videoserverurl=https://gateway-na.assetsadobe.com/DMGateway/public/demoCo&posterimage=/content/dam/marketing/shoppable-video/adobe-axis-demo/Adobe_AXIS_V3_GRADED-HD.mp4&VideoPlayer.ssl=on
   ```

   另請參閱[將URL連結到Web應用程式](https://docs.adobe.com/content/help/en/experience-manager-64/assets/dynamic/linking-urls-to-yourwebapplication.html)。

* 如果您使用內嵌程式碼發佈動態媒體視訊，請將`VideoPlayer.ssl`新增至內嵌程式碼片段中其他檢視器組態參數的清單。 例如，若要強制HTTPS視訊傳送，請依下列範例附加`&VideoPlayer.ssl=on`:

   ```
   <style type="text/css"> 
    #s7video_div.s7videoviewer{ 
      width:100%;  
      height:auto; 
    } 
   </style> 
   <script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/VideoViewer.js"></script> 
   <div id="s7video_div"></div> 
   <script type="text/javascript"> 
    var s7videoviewer = new s7viewers.VideoViewer({ 
     "containerId" : "s7video_div", 
     "params" : {  
      "VideoPlayer.ssl" : "on", 
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

   另請參閱[將視訊內嵌至網頁](https://docs.adobe.com/content/help/en/experience-manager-64/assets/dynamic/linking-urls-to-yourwebapplication.html)。

