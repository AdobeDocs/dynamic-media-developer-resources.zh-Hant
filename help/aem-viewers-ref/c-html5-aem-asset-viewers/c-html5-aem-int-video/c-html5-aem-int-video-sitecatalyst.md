---
title: 支援Adobe Analytics追蹤
description: HTML5 Video360 Viewer支援Adobe Analytics立即可用的追蹤功能。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User,Data Engineer,Data Architect
exl-id: 74a69d01-fa58-4d36-8598-992baf6ae11d
source-git-commit: ce1ac4938c7baf482c6c55a9ad13379153a3ec5b
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 0%

---

# 支援Adobe Analytics追蹤{#support-for-adobe-analytics-tracking}

HTML5 Video360 Viewer支援Adobe Analytics立即可用的追蹤功能。

若要啟用追蹤，請將適當的公司預設集名稱傳遞為`config2`引數。

依預設，檢視器會傳送單一追蹤HTTP要求至已設定的影像伺服器，其中包含檢視器型別和版本資訊。

## 自訂追蹤 {#section-cda48fc9730142d0bb3326bac7df3271}

若要與協力廠商分析系統整合，必須接聽`trackEvent`檢視器回呼，並視需要處理回呼函式的`eventInfo`引數。


下列程式碼為此類處理常式函式的範例：

```javascript {.line-numbers}
var video360Viewer = new s7viewers.Video360Viewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/space_station_360-AVS", 
 "serverurl":"https://s7d9.scene7.com/is/image/", 
 "videoserverurl":"https://s7d9.scene7.com/is/content/" 
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
   <th colname="col2" class="entry"> <p>已傳送…… </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">載入</span> </p> </td> 
   <td colname="col2"> <p>當檢視器先載入時。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">交換</span> </p> </td> 
   <td colname="col2"> <p>當使用<span class="codeph"> setAsset() </span> API在檢視器中交換資產時。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">播放</span> </p> </td> 
   <td colname="col2"> <p>播放開始時。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">暫停</span> </p> </td> 
   <td colname="col2"> <p>暫停播放時。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">停止</span> </p> </td> 
   <td colname="col2"> <p>當播放停止時。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">里程碑</span> </p> </td> 
   <td colname="col2"> <p>當播放達到以下里程碑之一時：0%、25%、50%、75%或100%。 </p> </td> 
  </tr> 
 </tbody> 
</table>
