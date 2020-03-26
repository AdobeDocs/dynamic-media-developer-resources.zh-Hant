---
description: Flyout檢視器支援Adobe Analytics立即追蹤。
seo-description: Flyout檢視器支援Adobe Analytics立即追蹤。
seo-title: 支援Adobe Analytics追蹤
solution: Experience Manager
title: 支援Adobe Analytics追蹤
topic: Dynamic media
uuid: ac5a2de9-6275-434f-ae09-a588f4a71aa6
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 支援Adobe Analytics追蹤{#support-for-adobe-analytics-tracking}

Flyout檢視器支援Adobe Analytics立即追蹤。

## 立即可用追蹤 {#section-ba994f079d0343c8ae48adffaa3195a3}

內嵌縮放檢視器 [!DNL Adobe Analytics] 支援立即追蹤。 若要啟用追蹤，請傳遞正確的公司預設集名稱作為 `config2` 參數。

檢視器也會傳送單一追蹤HTTP要求給已設定的影像伺服器，並包含檢視器類型和版本資訊。

## 自訂追蹤 {#section-cda48fc9730142d0bb3326bac7df3271}

若要與協力廠商分析系統整合，必須聽取檢視器回呼 `trackEvent` ，並視需要 `eventInfo` 處理回呼函式的引數。 以下代碼是此類處理程式函式的示例：

```
var inlineZoomViewer = new s7viewers.FlyoutViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
"config" : "Scene7SharedAssets/Universal_HTML5_Zoom_Inline", 
"contenturl" : "http://s7d1.scene7.com/is/content/", 
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
   <td colname="col2"> <p>資產會使用setAsset() <span class="codeph"> API在檢視器中 </span> 交換。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZOOM </span> </p> </td> 
   <td colname="col2"> <p>會啟動彈出畫面，或變更縮放等級。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PAN </span> </p> </td> 
   <td colname="col2"> <p> 影像被繪製。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SWATCH </span> </p> </td> 
   <td colname="col2"> <p> 通過按一下或點選色板更改影像。 </p> </td> 
  </tr> 
 </tbody> 
</table>

