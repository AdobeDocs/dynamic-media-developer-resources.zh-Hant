---
title: 支援Adobe Analytics追蹤
description: 支援Adobe Analytics追蹤
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User,Data Engineer,Data Architect
exl-id: 9e321684-4861-4d81-b55c-66c77635930e
source-git-commit: ce1ac4938c7baf482c6c55a9ad13379153a3ec5b
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 0%

---

# 支援Adobe Analytics追蹤{#support-for-adobe-analytics-tracking}

## 自訂追蹤 {#section-cda48fc9730142d0bb3326bac7df3271}

依預設，檢視器會傳送單一追蹤HTTP要求給已設定的影像伺服器，其中包含檢視器型別和版本資訊。

若要與協力廠商分析系統整合，必須接聽`trackEvent`檢視器回呼，並視需要處理回呼函式的`eventInfo`引數。

<!-- The following code is an example of such handler function: -->

<!--

```java {.line-numbers}
var carouselViewer = new s7viewers.CarouselViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner", 
 "serverurl":"https://adobedemo62-h.assetsadobe.com/is/image" 
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

-->

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
   <td colname="col1"> <p> <span class="codeph">載入</span> </p> </td> 
   <td colname="col2"> <p>首先載入檢視器。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">橫幅</span> </p> </td> 
   <td colname="col2"> <p>輪播橫幅影像已變更。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> HREF </span> </p> </td> 
   <td colname="col2"> <p>使用者會啟動熱點。 </p> </td> 
  </tr> 
 </tbody> 
</table>
