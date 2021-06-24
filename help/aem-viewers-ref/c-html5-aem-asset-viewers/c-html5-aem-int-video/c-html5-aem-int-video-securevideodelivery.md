---
description: HTTPS視訊傳送
solution: Experience Manager
title: HTTPS視訊傳送
feature: Dynamic Media Classic，檢視器， SDK/API，互動式影片
role: Developer,Business Practitioner
exl-id: 68d37b5d-5015-4a98-84b8-8911ace327ed
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 0%

---

# HTTPS視訊傳送{#https-video-delivery}

>[!NOTE]
>
>安全視訊傳送僅適用於安裝[Feature Pack-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480)的AEM 6.2，以及安裝[Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011)的AEM 6.1。

如果檢視器依本節開頭所述的設定運作，則發佈的視訊傳送可能會以HTTPS（安全）和HTTP（不安全）模式進行。 在預設配置中，視頻傳送協定嚴格遵守嵌入網頁的傳送協定。 不過，無論使用[VideoPlayer.ssl](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/r-html5-aem-int-video-config-attrib/r-html5-aem-int-video-config-attrib-videoplayer-ssl.md#reference-c28e1b700977493eadab5489458d7771)組態屬性內嵌網頁所使用的通訊協定為何，都可強制執行HTTPS視訊傳送。 （請注意，以製作模式預覽視訊的方式一律是透過HTTPS安全地傳送。）

根據您在AEM中使用的發佈Dynamic Media視訊的方法，`VideoPlayer.ssl`設定屬性的套用方式不同，如下所示：

* 如果您發佈含有URL的Dynamic Media影片，會將`VideoPlayer.ssl`附加至URL。 例如，為了強制安全視訊傳送，您將`&VideoPlayer.ssl=on`附加至下列檢視器URL範例的結尾：

   ```
   https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/InteractiveVideoViewer.html?asset=%2Fcontent%2Fdam%2Fmarketing%2Fshoppable-video%2Fadobe-axis-demo%2FAdobe_AXIS_V3_GRADED-HD.mp4&config=/etc/dam/presets/viewer/Shoppable_Video_light&serverUrl=https%3A%2F%2Fadobedemo62-h.assetsadobe.com%2Fis%2Fimage%2F&contenturl=%2F&config2=/etc/dam/presets/analytics&videoserverurl=https://gateway-na.assetsadobe.com/DMGateway/public/demoCo&interactivedata=content/dam/_VTT/marketing/shoppable-video/adobe-axis-demo/Adobe_AXIS_V3_GRADED-HD.mp4.svideo.vtt&VideoPlayer.contenturl=https://adobedemo62-h.assetsadobe.com/is/content&VideoPlayer.ssl=on
   ```

   另請參閱[將URL連結到Web應用程式](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html?lang=en#dynamic)

* 如果您使用內嵌程式碼發佈Dynamic Media視訊，請將`VideoPlayer.ssl`新增至內嵌程式碼片段中其他檢視器設定參數的清單。 例如，若要強制HTTPS視訊傳送，您需依下列範例附加`&VideoPlayer.ssl=on`:

   ```
   <style type="text/css"> 
    #s7interactivevideo_div.s7interactivevideoviewer{ 
      width:100%;  
      height:auto; 
    } 
   </style> 
   <script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script> 
   <div id="s7interactivevideo_div"></div> 
   <script type="text/javascript"> 
    var s7interactivevideoviewer = new s7viewers.InteractiveVideoViewer({ 
     "containerId" : "s7interactivevideo_div", 
     "params" : {  
      "VideoPlayer.ssl" : "on", 
      "serverurl" : "https://adobedemo62-h.assetsadobe.com/is/image", 
      "contenturl" : "https://demos-pub.assetsadobe.com/",  
      "config" : "/etc/dam/presets/viewer/Shoppable_Video_light", 
      "config2": "/etc/dam/presets/analytics", 
      "videoserverurl": "https://gateway-na.assetsadobe.com/DMGateway/public/demoCo", 
      "interactivedata": "content/dam/_VTT/marketing/shoppable-video/adobe-axis-demo/Adobe_AXIS_V3_GRADED-HD.mp4.svideo.vtt", 
      "VideoPlayer.contenturl": "https://adobedemo62-h.assetsadobe.com/is/content", 
      "asset" : "/content/dam/marketing/shoppable-video/adobe-axis-demo/Adobe_AXIS_V3_GRADED-HD.mp4" } 
    }) 
    /* // Example of interactive video event for quick view. 
      s7interactivevideoviewer.setHandlers({  
      "quickViewActivate": function(inData) { 
        var sku=inData.sku; //SKU for product ID 
       //To pass other parameter from the hotspot, you will need to add custom parameter during the hotspot setup as parameterName=value 
       loadQuickView(sku); //Replace this call with your quickview plugin 
       //Please refer to your quickviewer plugin for the quickview call 
       },  
   "initComplete":function() {  
       //--- Attach quickview popup to viewer container so popup will work in fullscreen mode --- 
       var popup = document.getElementById('quickview_div'); // get custom quick view container 
       popup.parentNode.removeChild(popup); // remove it from current DOM 
       var sdkContainerId = s7interactivevideoviewer.getComponent("container").getInnerContainerId(); // get viewer container component 
       var inner_container = document.getElementById(sdkContainerId);  
       inner_container.appendChild(popup); //Attach custom quick view container to viewer 
       }  
      }); 
    */ 
    s7interactivevideoviewer.init(); 
   </script>
   ```

   另請參閱[將視訊嵌入網頁](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html#dynamic)。
