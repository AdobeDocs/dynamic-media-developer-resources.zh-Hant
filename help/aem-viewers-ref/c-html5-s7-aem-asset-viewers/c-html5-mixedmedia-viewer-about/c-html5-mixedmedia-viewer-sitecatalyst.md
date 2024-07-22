---
title: 支援Adobe Analytics追蹤
description: 混合媒體檢視器可支援立即可用的Adobe Analytics追蹤功能。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User,Data Engineer,Data Architect
exl-id: 3b28c853-3747-4805-a141-3cce1398d783
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 0%

---

# 支援Adobe Analytics追蹤{#support-for-adobe-analytics-tracking}

混合媒體檢視器可支援立即可用的Adobe Analytics追蹤功能。

## 現成可用的追蹤 {#section-ba994f079d0343c8ae48adffaa3195a3}

混合媒體檢視器支援[!DNL Adobe Analytics]立即可用的追蹤。 若要啟用追蹤，請將適當的公司預設集名稱傳遞為`config2`引數。

檢視器也會將單一追蹤HTTP要求傳送至已設定的影像伺服器，並提供檢視器型別和版本資訊。

## 自訂追蹤 {#section-cda48fc9730142d0bb3326bac7df3271}

若要與協力廠商分析系統整合，必須接聽`trackEvent`檢視器回呼，並視需要處理回呼函式的`eventInfo`引數。 下列程式碼為此類處理常式函式的範例：

```javascript {.line-numbers}
var mixedMediaViewer = new s7viewers.MixedMediaViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Mixed_Media_Set_Sample", 
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
   <td colname="col2"> <p>影像會縮放。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">平移</span> </p> </td> 
   <td colname="col2"> <p>已平移影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">色票</span> </p> </td> 
   <td colname="col2"> <p> 按一下或點選色票即可變更影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">播放</span> </p> </td> 
   <td colname="col2"> <p>播放已開始。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">暫停</span> </p> </td> 
   <td colname="col2"> <p>播放已暫停。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">停止</span> </p> </td> 
   <td colname="col2"> <p>播放已停止。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">里程碑</span> </p> </td> 
   <td colname="col2"> <p>播放達到下列其中一個毫石： 0%、25%、50%、75%和100%。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">迴轉</span> </p> </td> 
   <td colname="col2"> <p>執行迴轉。 </p> </td> 
  </tr> 
 </tbody> 
</table>
