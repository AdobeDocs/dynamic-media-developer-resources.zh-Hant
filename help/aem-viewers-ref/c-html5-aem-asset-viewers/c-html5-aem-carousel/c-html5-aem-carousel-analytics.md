---
title: 支援Adobe Analytics跟蹤
description: 支援Adobe Analytics跟蹤
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User,Data Engineer,Data Architect
exl-id: 9e321684-4861-4d81-b55c-66c77635930e
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 1%

---

# 支援Adobe Analytics跟蹤{#support-for-adobe-analytics-tracking}

## 自定義跟蹤 {#section-cda48fc9730142d0bb3326bac7df3271}

預設情況下，查看器會向配置的Image Server發送一個跟蹤HTTP請求，其中包含查看器類型和版本資訊。

要與第三方分析系統整合，必須傾聽 `trackEvent` 查看器回調並處理 `eventInfo` 回調函式的參數。 以下代碼是此類處理程式函式的示例：

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

查看器跟蹤以下SDK用戶事件：

<table id="table_5D090E6614974D968E1A93B5727D859C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>SDK用戶事件 </p> </th> 
   <th colname="col2" class="entry"> <p>發送時間…… </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LOAD </span> </p> </td> 
   <td colname="col2"> <p>首先載入查看器。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 橫幅 </span> </p> </td> 
   <td colname="col2"> <p>旋轉木馬橫幅影像被更改。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> HREF </span> </p> </td> 
   <td colname="col2"> <p>用戶激活熱點。 </p> </td> 
  </tr> 
 </tbody> 
</table>
