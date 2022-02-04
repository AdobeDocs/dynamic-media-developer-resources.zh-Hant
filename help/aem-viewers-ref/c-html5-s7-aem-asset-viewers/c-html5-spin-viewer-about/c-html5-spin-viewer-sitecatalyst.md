---
title: Support for Adobe Analytics tracking
description: The Spin Viewer supports Adobe Analytics tracking out of the box.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User,Data Engineer,Data Architect
exl-id: 30762700-6d69-4299-9492-57893232abe1
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 3%

---

# 支援Adobe Analytics跟蹤{#support-for-adobe-analytics-tracking}

The Spin Viewer supports Adobe Analytics tracking out of the box.

## 現成跟蹤 {#section-d06145cfa2b9491bb485b599368d466e}

Spin Viewer支援Adobe Analytics開箱跟蹤。

要啟用跟蹤，請將正確的公司預設名稱作為 `config2` 的下界。

查看器還向配置的Image Server發送單個跟蹤HTTP請求，其中包含查看器類型和版本資訊。

## 自定義跟蹤 {#section-47512156a1d64b338b50cfa39c84f4aa}

To integrate with third-party analytics systems, it is necessary to listen to the `trackEvent` viewer callback and process the `eventInfo` argument of the callback function, as necessary. 以下代碼是此類處理程式函式的示例：

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

查看器跟蹤以下SDK用戶事件：

<table id="table_5D090E6614974D968E1A93B5727D859C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>SDK user event </p> </th> 
   <th colname="col2" class="entry"> <p>Sent when... </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LOAD </span> </p> </td> 
   <td colname="col2"> <p>viewer is loaded first. </p> </td> 
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
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SPIN </span> </p> </td> 
   <td colname="col2"> <p> 執行旋轉。 </p> </td> 
  </tr> 
 </tbody> 
</table>
