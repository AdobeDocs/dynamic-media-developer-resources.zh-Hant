---
title: 支援Adobe Analytics跟蹤
description: 支援Adobe Analytics跟蹤
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User,Data Engineer,Data Architect
exl-id: fb58a388-e4da-475d-b726-d5a32e99cce0
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 2%

---

# 支援Adobe Analytics跟蹤{#support-for-adobe-analytics-tracking}

預設情況下，查看器會向配置的Image Server發送單個跟蹤HTTP請求，其中包含查看器類型和版本資訊。

## 自定義跟蹤 {#section-cda48fc9730142d0bb3326bac7df3271}

為了與第三方分析系統整合，必須傾聽 `trackEvent` 查看器回調和進程 `eventInfo` 回調函式的參數。 以下代碼是此類處理程式函式的示例：

```javascript {.line-numbers}
var panoramicViewer = new s7viewers.PanoramicViewer({
	"containerId":"s7viewer",
"params":{
	"asset":"Scene7SharedAssets/PanoramicImage-Sample",
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
   <th colname="col2" class="entry"> <p>已傳送... </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LOAD </span> </p> </td> 
   <td colname="col2"> <p>的下界。 </p> </td> 
  </tr> 
 </tbody> 
</table>
