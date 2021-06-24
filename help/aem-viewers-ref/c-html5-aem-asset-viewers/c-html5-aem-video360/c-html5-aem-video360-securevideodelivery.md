---
description: HTTPS視訊傳送
solution: Experience Manager
title: HTTPS視訊傳送
feature: Dynamic Media Classic，檢視器，SDK/API,360 VR影片
role: Developer,Business Practitioner
exl-id: 79f7e356-55d1-46e1-b85a-2e73633c9404
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '287'
ht-degree: 0%

---

# HTTPS視訊傳送{#https-video-delivery}

>[!NOTE]
>
>HTTP安全視訊傳送僅適用於安裝[Feature Pack-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480)的AEM 6.2，以及安裝[Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011)的AEM 6.1。

如果檢視器依本節開頭所述的設定運作，則發佈的視訊傳送可能會以HTTPS（安全）和HTTP（不安全）模式進行。 在預設配置中，視頻傳送協定嚴格遵守嵌入網頁的傳送協定。 不過，無論使用[Video360Player.ssl](/help/aem-viewers-ref/c-html5-aem-asset-viewers/c-html5-aem-video360/r-html5-aem-video360-config-attrib/r-html5-aem-video360-config-attrib-video360player-ssl.md)設定屬性內嵌網頁所使用的通訊協定為何，都可強制執行HTTPS視訊傳送。 （請注意，以製作模式預覽視訊的方式一律是透過HTTPS安全地傳送。）

根據您在AEM中使用的發佈Dynamic Media視訊的方法，`Video360Player.ssl`設定屬性的套用方式不同，如下所示：

* 如果您發佈含有URL的Dynamic Media影片，會將`Video360Player.ssl`附加至URL。 例如，為了強制安全視訊傳送，您將`&Video360Player.ssl=on`附加至下列檢視器URL範例的結尾：

   ```
   https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/Video360Viewer.html?asset=%2Fcontent%2Fdam%2Fmarketing%2Fshoppable-video%2Fadobe-axis-demo%2FAdobe_AXIS_V3_GRADED-HD.mp4&config=/etc/dam/presets/viewer/Video&serverUrl=https%3A%2F%2Fadobedemo62-h.assetsadobe.com%2Fis%2Fimage%2F&contenturl=%2F&config2=/etc/dam/presets/analytics&videoserverurl=https://gateway-na.assetsadobe.com/DMGateway/public/demoCo&posterimage=/content/dam/marketing/shoppable-video/adobe-axis-demo/Adobe_AXIS_V3_GRADED-HD.mp4&Video360Player.ssl=on
   ```

   另請參閱[將URL連結到Web應用程式](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html?lang=en#dynamic)。

* 如果您使用內嵌程式碼發佈Dynamic Media視訊，請將`Video360Player.ssl`新增至內嵌程式碼片段中其他檢視器設定參數的清單。 例如，若要強制HTTPS視訊傳送，您需依下列範例附加`&Video360Player.ssl=on`:

   ```
   <style type="text/css"> 
    #s7video_div.s7video360viewer{ 
      width:100%;  
      height:auto; 
    } 
   </style> 
   <script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/Video360Viewer.js"></script> 
   <div id="s7video_div"></div> 
   <script type="text/javascript"> 
    var s7video360viewer = new s7viewers.Video360Viewer({ 
     "containerId" : "s7video_div", 
     "params" : {  
      "Video360Player.ssl" : "on", 
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

   另請參閱[將視訊嵌入網頁](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html#dynamic)
