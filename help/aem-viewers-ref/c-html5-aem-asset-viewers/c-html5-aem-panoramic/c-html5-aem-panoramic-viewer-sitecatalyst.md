---
title: 支援Adobe Analytics追蹤
description: 支援Adobe Analytics追蹤
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User,Data Engineer,Data Architect
exl-id: fb58a388-e4da-475d-b726-d5a32e99cce0
source-git-commit: 8aebcacd5abdc23565aab1bc3506c36f055b6439
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 2%

---

# 支援Adobe Analytics追蹤{#support-for-adobe-analytics-tracking}

依預設，檢視器會傳送單一追蹤HTTP要求至已設定的影像伺服器，並附上檢視器類型和版本資訊。

## 自訂追蹤 {#section-cda48fc9730142d0bb3326bac7df3271}

若要與協力廠商分析系統整合，必須監聽 `trackEvent` 檢視器回呼及處理 `eventInfo` 回呼函式的引數。 以下代碼是此類處理程式函式的示例：

```
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

檢視器會追蹤下列SDK使用者事件：

<table id="table_5D090E6614974D968E1A93B5727D859C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>SDK使用者事件 </p> </th> 
   <th colname="col2" class="entry"> <p>已傳送... </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LOAD </span> </p> </td> 
   <td colname="col2"> <p>檢視器先載入時。 </p> </td> 
  </tr> 
 </tbody> 
</table>
