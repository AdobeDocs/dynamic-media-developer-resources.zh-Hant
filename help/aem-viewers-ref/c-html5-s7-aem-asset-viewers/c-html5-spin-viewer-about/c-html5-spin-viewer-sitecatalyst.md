---
title: 支援Adobe Analytics追蹤
description: 迴轉檢視器支援立即可用的Adobe Analytics追蹤。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 30762700-6d69-4299-9492-57893232abe1
TQID: 'https://experienceleague.adobe.com/a9Ab9GwdXqTOrBLuKj49d5Jl01V2-iGH5xb1khFGH7g'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 163
ht-degree: 0%

---

# 支援Adobe Analytics追蹤{#support-for-adobe-analytics-tracking}

迴轉檢視器支援立即可用的Adobe Analytics追蹤。

## 現成可用的追蹤 {#section-d06145cfa2b9491bb485b599368d466e}

迴轉檢視器支援Adobe Analytics立即可用追蹤。

若要啟用追蹤，請將適當的公司預設集名稱傳遞為`config2`引數。

檢視器也會將單一追蹤HTTP要求傳送至已設定的影像伺服器，並提供檢視器型別和版本資訊。

## 自訂追蹤 {#section-47512156a1d64b338b50cfa39c84f4aa}

若要與協力廠商分析系統整合，必須接聽`trackEvent`檢視器回呼，並視需要處理回呼函式的`eventInfo`引數。 下列程式碼為此類處理常式函式的範例：

```javascript {.line-numbers}
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
  <tr> 
   <td colname="col1"> <p> <span class="codeph">迴轉</span> </p> </td> 
   <td colname="col2"> <p> 執行迴轉。 </p> </td> 
  </tr> 
 </tbody> 
</table>
