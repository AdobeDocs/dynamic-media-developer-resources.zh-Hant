---
title: 全景查看器
description: 建構子，建立新的HTML5 Carousel查看器實例。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 3%

---

# 全景查看器{#panoramicviewer}

`PanoramicViewer([config])`
建構子，建立新的HTML5 Panoramic Viewer實例。

## 參數 {#section-fa807db629ce43bab286b1e1dc96c492}

config {Object}可選JSON配置對象，允許將所有查看器設定傳遞給建構子，並避免調用單個setter方法。 包含以下屬性：
* containerId — 插入查看器的DOM容器（通常為DIV）的{String} ID。 不必在調用此方法時建立容器元素，但執行init()時必須存在容器。 必要
* params - {Object} JSON對象，帶有查看器配置參數，其中屬性名稱是特定於查看器的配置選項或SDK修飾符，該屬性的值是相應的設定值。 必要
* 處理程式 — 具有查看器事件回調的{Object} JSON對象，其中屬性名稱是支援的查看器事件的名稱，屬性值是對相應回調的JavaScript函式引用。 有關查看器事件的詳細資訊，請參閱「事件回調」部分。 選擇性


## 返回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

無。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```javascript {.line-numbers}
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
