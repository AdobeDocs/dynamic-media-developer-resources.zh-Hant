---
title: 支援Adobe Analytics跟蹤
description: 視頻查看器支援Adobe Analytics開箱跟蹤。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User,Data Engineer,Data Architect
exl-id: 2cc7087d-ed02-4560-b9ce-533af2b11a24
source-git-commit: 11acb9151d3ea247eecde3cfbbd295a95c10829c
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 3%

---

# 支援Adobe Analytics跟蹤{#support-for-adobe-analytics-tracking}

視頻查看器支援Adobe Analytics開箱跟蹤。

## 現成跟蹤 {#section-3b101fe30be943c1b679fd5c273569ca}

視頻查看器支援Adobe Analytics開箱跟蹤。

要啟用跟蹤，請將正確的公司預設名稱作為 `config2` 的下界。

查看器還向配置的Image Server發送單個跟蹤HTTP請求，其中包含查看器類型和版本資訊。

## 自定義跟蹤 {#section-ab10bd7caf184721a366cf3953071934}

要與第三方分析系統整合，必須傾聽 `trackEvent` 查看器回調和進程 `eventInfo` 回調函式的參數。 以下代碼是此類處理程式函式的示例：

```
var videoViewer = new s7viewers.VideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Glacier_Climber_MP4", 
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
   <td colname="col1"> <p> <span class="codeph"> PLAY </span> </p> </td> 
   <td colname="col2"> <p>播放。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PAUSE </span> </p> </td> 
   <td colname="col2"> <p>播放已暫停。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> STOP </span> </p> </td> 
   <td colname="col2"> <p>播放已停止。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MILESTONE </span> </p> </td> 
   <td colname="col2"> <p>播放到以下「millstones（重放）」之一：0%,25%,50%,75%和100%。 </p> </td> 
  </tr> 
 </tbody> 
</table>
