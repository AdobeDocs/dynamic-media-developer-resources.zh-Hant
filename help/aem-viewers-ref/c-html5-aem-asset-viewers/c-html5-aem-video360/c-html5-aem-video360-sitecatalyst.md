---
description: 支援Adobe Analytics追蹤
solution: Experience Manager
title: 支援Adobe Analytics追蹤
feature: Dynamic Media經典，檢視器，SDK/API,360 VR視訊
role: 開發人員，商業從業人員，資料工程師，資料架構師
exl-id: fb58a388-e4da-475d-b726-d5a32e99cce0
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 4%

---

# 支援Adobe Analytics追蹤{#support-for-adobe-analytics-tracking}

依預設，檢視器會傳送單一追蹤HTTP要求給已設定的影像伺服器，並包含檢視器類型和版本資訊。

## 自訂追蹤{#section-cda48fc9730142d0bb3326bac7df3271}

若要與協力廠商分析系統整合，必須監聽`trackEvent`檢視器回呼，並視需要處理回呼函式的`eventInfo`引數。 以下代碼是此類處理程式函式的示例：

```
var interactiveVideoViewer = new s7viewers.InteractiveVideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4", 
"config":"/etc/dam/presets/viewer/Shoppable_Video_Dark", 
 "serverurl":"https://aodmarketingna.assetsadobe.com/is/image/", 
 "videoserverurl":"https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna", 
 "contenturl":"https://aodmarketingna.assetsadobe.com/", 
"interactivedata":"is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt" 
}, 
"handlers":{ 
 "trackEvent":function(objID, compClass, instName, timeStamp, eventInfo) { 
  //identify event type 
  var eventType = eventInfo.split(",")[0]; 
  switch (eventType) { 
   case "LOAD": 
    //custom event processing code 
    break; 
   case "INTERACTIVE_SWATCH": 
    //custom event processing code which handles user clicks on interactive swatches 
    break; 
   //additional cases for other events 
} 
} 
} 
});
```

檢視器會追蹤下列SDK使用者事件：

<table id="table_5D090E6614974D968E1A93B5727D859C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>SDK使用者事件 </p> </th> 
   <th colname="col2" class="entry"> <p>已傳送... </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LOAD </span> </p> </td> 
   <td colname="col2"> <p>當檢視器先載入時。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SWAP </span> </p> </td> 
   <td colname="col2"> <p>使用<span class="codeph"> setAsset()</span> API在檢視器中交換資產時。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PLAY </span> </p> </td> 
   <td colname="col2"> <p>播放開始時。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PAUSE </span> </p> </td> 
   <td colname="col2"> <p>播放暫停時。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> STOP </span> </p> </td> 
   <td colname="col2"> <p>當播放停止時。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MILESTONE </span> </p> </td> 
   <td colname="col2"> <p>播放到達下列里程碑之一時：0%、25%、50%、75%或100%。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> INTERACTIVE_SWATCH  </span> </p> </td> 
   <td colname="col2"> <p>每次使用者按互動式色票時。 </p> </td> 
  </tr> 
 </tbody> 
</table>
