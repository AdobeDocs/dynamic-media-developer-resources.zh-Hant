---
title: 支援Adobe Analytics跟蹤
description: 「基本縮放查看器」支援Adobe Analytics從框中跟蹤。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User,Data Engineer,Data Architect
exl-id: 5b9d871d-9f37-4908-900e-3f0ecc98bc0c
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 2%

---

# 支援Adobe Analytics跟蹤{#support-for-adobe-analytics-tracking}

「基本縮放查看器」支援Adobe Analytics從框中跟蹤。

## 現成跟蹤 {#section-ba994f079d0343c8ae48adffaa3195a3}

基本縮放查看器支援 [!DNL Adobe Analytics] 追蹤現場。 要啟用跟蹤，請將正確的公司預設名稱作為 `config2` 的下界。

查看器還向配置的Image Server發送單個跟蹤HTTP請求，其中包含查看器類型和版本資訊。

## 自定義跟蹤 {#section-cda48fc9730142d0bb3326bac7df3271}

要與第三方分析系統整合，必須傾聽 `trackEvent` 查看器回調並處理 `eventInfo` 回調函式的參數。 以下代碼是此類處理程式函式的示例：

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
   <td colname="col1"> <p> <span class="codeph"> SWAP </span> </p> </td> 
   <td colname="col2"> <p>在查看器中使用 <span class="codeph"> setAsset() </span> API。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZOOM </span> </p> </td> 
   <td colname="col2"> <p> 縮放影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PAN </span> </p> </td> 
   <td colname="col2"> <p>一幅圖畫被繪製。 </p> </td> 
  </tr> 
 </tbody> 
</table>
