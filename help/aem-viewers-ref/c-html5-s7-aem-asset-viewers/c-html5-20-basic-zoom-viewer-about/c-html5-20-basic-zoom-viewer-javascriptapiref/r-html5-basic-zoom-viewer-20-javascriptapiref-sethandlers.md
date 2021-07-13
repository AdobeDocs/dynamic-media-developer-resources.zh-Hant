---
description: 基本縮放檢視器的JavaScript API參考
solution: Experience Manager
title: setHandlers
feature: Dynamic Media Classic，檢視器，SDK/API，縮放
role: Developer,User
exl-id: d800dbbc-2c40-4911-8f29-c8413847f7be
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 3%

---

# setHandlers{#sethandlers}

基本縮放檢視器的JavaScript API參考

`setHandlers(handlers)`

指定零個或多個回調處理程式。 對此方法的呼叫會完全覆寫先前為該檢視器例項指派的事件處理常式。 必須在`init()`之前呼叫。

## 參數 {#section-b60f082cca1542748b605689b1d43f8a}

<table id="table_98A620DAE2C340FA97BF7204AE023CC8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 處理器  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 具有查看 </span> 器事件回呼的{Object} JSON物件，其中屬性名稱是受支援的查看器事件的名稱，屬性值是適當回呼的JavaScript函式參考。 </p> <p>如需檢視器事件的詳細資訊，請參閱<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-event-callbacks.md#concept-8ba57cf86537401999514e1b221ec734" format="dita" scope="local">事件回呼</a> 。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 傳回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

無。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
})
```
