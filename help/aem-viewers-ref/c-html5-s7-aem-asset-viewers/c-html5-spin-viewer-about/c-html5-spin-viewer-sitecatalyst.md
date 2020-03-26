---
description: 回轉檢視器支援Adobe Analytics立即追蹤。
seo-description: 回轉檢視器支援Adobe Analytics立即追蹤。
seo-title: 支援Adobe Analytics追蹤
solution: Experience Manager
title: 支援Adobe Analytics追蹤
topic: Dynamic media
uuid: 337671f0-22e8-4e3e-a0a9-ce49d271ea56
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 支援Adobe Analytics追蹤{#support-for-adobe-analytics-tracking}

回轉檢視器支援Adobe Analytics立即追蹤。

## 立即可用追蹤 {#section-d06145cfa2b9491bb485b599368d466e}

回轉檢視器支援Adobe Analytics立即可用追蹤。

若要啟用追蹤，請傳遞正確的公司預設集名稱作為 `config2` 參數。

檢視器也會傳送單一追蹤HTTP要求給已設定的影像伺服器，並包含檢視器類型和版本資訊。

## 自訂追蹤 {#section-47512156a1d64b338b50cfa39c84f4aa}

若要與協力廠商分析系統整合，必須聽取檢視器回呼 `trackEvent` ，並視需要 `eventInfo` 處理回呼函式的引數。 以下代碼是此類處理程式函式的示例：

```
var spinViewer = new s7viewers.SpinViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/SpinSet_Sample", 
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
   <td colname="col2"> <p> 放大影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PAN </span> </p> </td> 
   <td colname="col2"> <p>影像被繪製。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SPIN </span> </p> </td> 
   <td colname="col2"> <p> 執行旋轉。 </p> </td> 
  </tr> 
 </tbody> 
</table>

