---
title: HTTPS視訊傳送
description: HTTPS視訊傳送
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 68d37b5d-5015-4a98-84b8-8911ace327ed
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 0%

---

# HTTPS視訊傳送{#https-video-delivery}

<!-- >[!NOTE]
>
>Secure Video Delivery only applies to AEM 6.2 with the installation of [Feature Pack-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) and to AEM 6.1 with installation of [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011). -->

如果檢視器的設定如本節開頭所述，則發佈的視訊傳送可能會以HTTPS（安全）和HTTP（不安全）模式進行。 在預設配置中，視頻傳送協定嚴格遵守嵌入網頁的傳送協定。 不過，強制HTTPS視訊傳送是可能的，而不考慮透過內嵌網頁所使用的通訊協定 [VideoPlayer.ssl](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/r-html5-aem-int-video-config-attrib/r-html5-aem-int-video-config-attrib-videoplayer-ssl.md#reference-c28e1b700977493eadab5489458d7771) 配置屬性。 （在製作模式中的視訊預覽一律會透過HTTPS安全地傳送。）

視發佈方法而定 [!DNL Dynamic Media] 在Adobe Experience Manager中使用的影片， `VideoPlayer.ssl` 設定屬性的套用方式不同，如下所示：

* 若您發佈 [!DNL Dynamic Media] 含有URL的影片，您會附加 `VideoPlayer.ssl` 至URL。 例如，為了強制傳送安全視訊，您會附加 `&VideoPlayer.ssl=on` 到下列檢視器URL範例的結尾：

   ```
   https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/InteractiveVideoViewer.html?asset=%2Fcontent%2Fdam%2Fmarketing%2Fshoppable-video%2Fadobe-axis-demo%2FAdobe_AXIS_V3_GRADED-HD.mp4&config=/etc/dam/presets/viewer/Shoppable_Video_light&serverUrl=https%3A%2F%2Fadobedemo62-h.assetsadobe.com%2Fis%2Fimage%2F&contenturl=%2F&config2=/etc/dam/presets/analytics&videoserverurl=https://gateway-na.assetsadobe.com/DMGateway/public/demoCo&interactivedata=content/dam/_VTT/marketing/shoppable-video/adobe-axis-demo/Adobe_AXIS_V3_GRADED-HD.mp4.svideo.vtt&VideoPlayer.contenturl=https://adobedemo62-h.assetsadobe.com/is/content&VideoPlayer.ssl=on
   ```

   另請參閱 [將URL連結至您的Web應用程式](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html?lang=en#dynamic)

* 若您發佈 [!DNL Dynamic Media] 含有內嵌程式碼的視訊，您新增 `VideoPlayer.ssl` 內嵌程式碼片段中其他檢視器設定參數的清單。 例如，若要強制HTTPS視訊傳送，請附加 `&VideoPlayer.ssl=on` 如下列範例：

   ```html {.line-numbers}
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

   另請參閱 [將視訊內嵌在網頁上](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html#dynamic).
