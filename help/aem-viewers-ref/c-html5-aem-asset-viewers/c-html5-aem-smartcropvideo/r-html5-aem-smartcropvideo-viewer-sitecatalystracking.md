---
description: 智慧型裁切視訊檢視器支援Adobe Analytics立即可用追蹤。
solution: Experience Manager
title: 支援Adobe Analytics追蹤
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User,Data Engineer,Data Architect
exl-id: 2cc7087d-ed02-4560-b9ce-533af2b11a24
source-git-commit: bdef251dcbb7c135d02813e9fd82e2e5e32300cc
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 3%

---

# 支援Adobe Analytics追蹤{#support-for-adobe-analytics-tracking}

智慧型裁切視訊檢視器支援Adobe Analytics立即可用追蹤。

## 現成可用追蹤 {#section-3b101fe30be943c1b679fd5c273569ca}

智慧型裁切視訊檢視器支援Adobe Analytics立即可用追蹤。

若要啟用追蹤，請將正確的公司預設集名稱傳遞為 `config2` 參數。

檢視器也會傳送單一追蹤HTTP要求至已設定的影像伺服器，並附上檢視器類型和版本資訊。

## 自訂追蹤 {#section-ab10bd7caf184721a366cf3953071934}

若要與協力廠商分析系統整合，必須監聽 `trackEvent` 檢視器回呼及處理 `eventInfo` 回呼函式的引數。 以下代碼是此類處理程式函式的示例：

```
var smartCropVideoViewer = new s7viewers.SmartCropVideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"html5automation/frisbee-AVS", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
}, 
"handlers":{ 
 "trackEvent":function(objID, compClass, instName, timeStamp, eventInfo) { 
  //identify event type 
  var eventType = eventInfo.split(",")[0]; 
  switch (eventType) { 
   case "LOAD": 
    //custom event processing code 
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
   <th colname="col2" class="entry"> <p>傳送時間…… </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LOAD </span> </p> </td> 
   <td colname="col2"> <p>檢視器會先載入。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SWAP </span> </p> </td> 
   <td colname="col2"> <p>在檢視器中，會使用 <span class="codeph"> setAsset() </span> API。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PLAY </span> </p> </td> 
   <td colname="col2"> <p>播放已開始。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PAUSE </span> </p> </td> 
   <td colname="col2"> <p>播放已暫停。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> STOP </span> </p> </td> 
   <td colname="col2"> <p>播放已停止。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MILESTONE </span> </p> </td> 
   <td colname="col2"> <p>播放達到下列其中一項：0%、25%、50%、75%和100%。 </p> </td> 
  </tr> 
 </tbody> 
</table>
