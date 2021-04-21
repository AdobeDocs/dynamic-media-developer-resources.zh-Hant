---
description: 視訊檢視器支援Adobe Analytics立即追蹤。
solution: Experience Manager
title: 支援Adobe Analytics追蹤
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,Business Practitioner,Data Engineer,Data Architect
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 3%

---


# 支援Adobe Analytics追蹤{#support-for-adobe-analytics-tracking}

視訊檢視器支援Adobe Analytics立即追蹤。

## 立即可用的追蹤{#section-3b101fe30be943c1b679fd5c273569ca}

視訊檢視器支援Adobe Analytics立即追蹤。

若要啟用追蹤，請將正確的公司預設集名稱傳遞為`config2`參數。

檢視器也會傳送單一追蹤HTTP要求給已設定的影像伺服器，並包含檢視器類型和版本資訊。

## 自訂追蹤{#section-ab10bd7caf184721a366cf3953071934}

若要與協力廠商分析系統整合，必須監聽`trackEvent`檢視器回呼，並視需要處理回呼函式的`eventInfo`引數。 以下代碼是此類處理程式函式的示例：

```
var videoViewer = new s7viewers.VideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Glacier_Climber_MP4", 
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
   <th colname="col2" class="entry"> <p>在…… </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LOAD </span> </p> </td> 
   <td colname="col2"> <p>檢視器會先載入。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SWAP </span> </p> </td> 
   <td colname="col2"> <p>使用<span class="codeph"> setAsset()</span> API在檢視器中交換資產。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PLAY </span> </p> </td> 
   <td colname="col2"> <p>播放開始。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PAUSE </span> </p> </td> 
   <td colname="col2"> <p>播放暫停。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> STOP </span> </p> </td> 
   <td colname="col2"> <p>播放已停止。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MILESTONE </span> </p> </td> 
   <td colname="col2"> <p>播放到以下重點之一：0%、25%、50%、75%和100%。 </p> </td> 
  </tr> 
 </tbody> 
</table>

