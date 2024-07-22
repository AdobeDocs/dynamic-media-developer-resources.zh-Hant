---
title: 支援Adobe Analytics追蹤
description: 基本縮放檢視器支援立即可用的Adobe Analytics追蹤。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User,Data Engineer,Data Architect
exl-id: 5b9d871d-9f37-4908-900e-3f0ecc98bc0c
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 0%

---

# 支援Adobe Analytics追蹤{#support-for-adobe-analytics-tracking}

基本縮放檢視器支援立即可用的Adobe Analytics追蹤。

## 現成可用的追蹤 {#section-ba994f079d0343c8ae48adffaa3195a3}

基本縮放檢視器支援[!DNL Adobe Analytics]立即可用的追蹤。 若要啟用追蹤，請將適當的公司預設集名稱傳遞為`config2`引數。

檢視器也會將單一追蹤HTTP要求傳送至已設定的影像伺服器，並提供檢視器型別和版本資訊。

## 自訂追蹤 {#section-cda48fc9730142d0bb3326bac7df3271}

若要與協力廠商分析系統整合，必須接聽`trackEvent`檢視器回呼，並視需要處理回呼函式的`eventInfo`引數。 下列程式碼為此類處理常式函式的範例：

```javascript {.line-numbers}
var basicZoomViewer = new s7viewers.BasicZoomViewer({ 
 "containerId":"s7viewer", 
 "params":{ 
  "asset":"Scene7SharedAssets/Backpack_B", 
  "serverurl":"http://s7d1.scene7.com/is/image/" 
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
   <td colname="col1"> <p> <span class="codeph">載入</span> </p> </td> 
   <td colname="col2"> <p>檢視器會先載入。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">交換</span> </p> </td> 
   <td colname="col2"> <p>在檢視器中使用<span class="codeph"> setAsset() </span> API交換資產。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">縮放</span> </p> </td> 
   <td colname="col2"> <p> 影像會縮放。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">平移</span> </p> </td> 
   <td colname="col2"> <p>已平移影像。 </p> </td> 
  </tr> 
 </tbody> 
</table>
