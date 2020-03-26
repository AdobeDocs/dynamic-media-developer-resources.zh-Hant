---
description: 'null'
seo-description: 'null'
seo-title: 支援分析追蹤
solution: Experience Manager
title: 支援分析追蹤
topic: Dynamic media
uuid: ae870d2e-2a09-4551-935a-916d0e657653
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 支援分析追蹤{#support-for-analytics-tracking}

## 自訂追蹤 {#section-cda48fc9730142d0bb3326bac7df3271}

依預設，檢視器會傳送單一追蹤HTTP要求至已設定的影像伺服器，並包含檢視器類型和版本資訊。

若要與協力廠商分析系統整合，必須聽取檢視器回呼 `trackEvent` ，並視需要處 `eventInfo` 理回呼函式的引數。 以下代碼是此類處理程式函式的示例：

```
var interactiveImage = new s7viewers.InteractiveImage({ 
 "containerId":"s7viewer", 
 "params":{ 
  "asset":"/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg", 
  "serverurl":"http://aodmarketingna.assetsadobe.com/is/image" 
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
   <th colname="col2" class="entry"> <p>在…… </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LOAD </span> </p> </td> 
   <td colname="col2"> <p>檢視器會先載入。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> HREF </span> </p> </td> 
   <td colname="col2"> <p>用戶激活熱點。 </p> </td> 
  </tr> 
 </tbody> 
</table>

