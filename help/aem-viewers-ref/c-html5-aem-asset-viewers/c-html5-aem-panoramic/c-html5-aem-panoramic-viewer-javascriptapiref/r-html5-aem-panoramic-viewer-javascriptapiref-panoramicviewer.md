---
title: PanoramicViewer
description: 建構函式會建立新的HTML5輪播檢視器例項。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
source-git-commit: 2dc7b92da6c73a328a82c50dc5a052a3351ee2dc
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 3%

---

# PanoramicViewer{#panoramicviewer}

`PanoramicViewer([config])`
建構子，建立新的HTML5 Panoramic Viewer實例。

## 參數 {#section-fa807db629ce43bab286b1e1dc96c492}

配置{object}可選JSON配置對象，允許將所有查看器設定傳遞給建構子，並避免調用單個setter方法。 包含下列屬性：
* containerId — 將插入檢視器的DOM容器（通常是DIV）的{String} ID。 不需要在調用此方法時建立容器元素，但執行init()時必須存在容器。 必要
* params - {Object} JSON物件與檢視器設定參數，其中屬性名稱為檢視器專屬組態選項或SDK修飾元，而該屬性的值是對應的設定值。 必要
* 處理程式 — 具有查看器事件回呼的{Object} JSON物件，其中屬性名稱是受支援的查看器事件的名稱，屬性值是適當回呼的JavaScript函式參考。 如需檢視器事件的詳細資訊，請參閱事件回呼區段。 選擇性


## 傳回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

無。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
var panoramicViewer = new s7viewers.PanoramicViewer({
	"containerId":"s7viewer",
"params":{
	"asset":"Scene7SharedAssets/PanoramicImage-Sample",
	"serverurl":"http://s7d1.scene7.com/is/image/"
},
"handlers":{
	"initComplete":function() {
		console.log("init complete");
}
}
});
```
