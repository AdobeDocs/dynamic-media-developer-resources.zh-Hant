---
description: 回轉檢視器的JavaScript API參考
solution: Experience Manager
title: setHandlers
feature: Dynamic Media經典，檢視器，SDK/API，回轉集
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 3%

---


# setHandlers{#sethandlers}

回轉檢視器的JavaScript API參考

`setHandlers(handlers)`

指定零個或多個回呼處理常式。 對此方法的呼叫會完全覆寫先前為該檢視器例項指派的事件處理常式。 必須在`init()`之前呼叫。

## 參數 {#section-51f820ded5e842bebd123e37a35176c7}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 處理程式  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object}  </span> JSON物件與檢視器事件回呼，其中屬性名稱是支援之檢視器事件的名稱，屬性值是適當回呼的JavaScript函式參考。 </p> <p>如需檢視器事件的詳細資訊，請參閱<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-event-callbacks.md#concept-9c553c80eefd422faacf6522c69804bf" format="dita" scope="local">事件回呼</a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 傳回{#section-1d3cf85bc7cc4dfe9670e038d02b9101}

無。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
})
```

