---
description: 「基本縮放檢視器」支援Adobe Analytics立即追蹤。
seo-description: 「基本縮放檢視器」支援Adobe Analytics立即追蹤。
seo-title: 支援Adobe Analytics追蹤
solution: Experience Manager
title: 支援Adobe Analytics追蹤
topic: Dynamic media
uuid: f48fde77-7e48-4d56-b5c5-079a484e6d9c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# 支援Adobe Analytics追蹤{#support-for-adobe-analytics-tracking}

「基本縮放檢視器」支援Adobe Analytics立即追蹤。

## 立即可用的追蹤{#section-ba994f079d0343c8ae48adffaa3195a3}

基本縮放檢視器支援[!DNL Adobe Analytics]立即追蹤。 若要啟用追蹤，請將正確的公司預設集名稱傳遞為`config2`參數。

檢視器也會傳送單一追蹤HTTP要求給已設定的影像伺服器，並包含檢視器類型和版本資訊。

## 自訂追蹤{#section-cda48fc9730142d0bb3326bac7df3271}

若要與協力廠商分析系統整合，必須監聽`trackEvent`檢視器回呼，並視需要處理回呼函式的`eventInfo`引數。 以下代碼是此類處理程式函式的示例：

```
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
   <td colname="col2"> <p>資產會使用<span class="codeph"> setAsset()</span> API在檢視器中交換。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZOOM </span> </p> </td> 
   <td colname="col2"> <p> 放大影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PAN </span> </p> </td> 
   <td colname="col2"> <p>影像被繪製。 </p> </td> 
  </tr> 
 </tbody> 
</table>

