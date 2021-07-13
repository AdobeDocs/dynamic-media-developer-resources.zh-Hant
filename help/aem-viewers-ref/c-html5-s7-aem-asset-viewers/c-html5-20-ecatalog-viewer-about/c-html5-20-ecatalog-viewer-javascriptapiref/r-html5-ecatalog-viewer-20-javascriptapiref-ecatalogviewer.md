---
description: eCatalog檢視器的JavaScript API參考。
solution: Experience Manager
title: eCatalogViewer
feature: Dynamic Media Classic，檢視器，SDK/API,eCatalog
role: Developer,User
exl-id: 111699a3-8a70-4caf-b7da-7b594b785f7c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 3%

---

# eCatalogViewer{#ecatalogviewer}

eCatalog檢視器的JavaScript API參考。

`eCatalogViewer([config])`

建構子，建立新的eCatalog查看器實例。

## 參數 {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 設定  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object}可 </span> 選JSON配置對象，允許所有查看器設定傳遞到建構子，並避免調用單個setter方法。包含下列屬性： </p> <p> 
     <ul id="ul_266C711E8E75471E90C15F39A96A142F"> 
      <li id="li_71857BBD652243A094E936C2C8EA9702"> <p> <span class="codeph"> containerId  </span> -  <span class="codeph"> { </span> String} DOM容器(通常是 <span class="codeph"> DIV </span>)的ID。呼叫此方法時，不需要建立容器元素。 但是，當<span class="codeph"> init()</span>運行時，容器必須存在。 必要. </p> </li> 
      <li id="li_3D28979F04274AC9B507B33D4275FC3A"> <p> <span class="codeph"> 參 </span> 數 —  <span class="codeph"> {Object}  </span> JSON物件及檢視器設定參數，其中屬性名稱為檢視器專屬組態選項或SDK修飾元，而該屬性的值為對應的設定值。必要. </p> </li> 
      <li id="li_A40AC2167575415FB3383D070E27B9AB"> <p> <span class="codeph"> 處理 </span> 程式 —  <span class="codeph"> {Object} JSON物 </span> 件，具有檢視器事件回呼，其中屬性名稱是支援的檢視器事件的名稱，而屬性值是適當回呼的JavaScript函式參考。選填。 </p> <p>如需檢視器事件的詳細資訊，請參閱<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-event-callbacks.md#concept-0bf5ff877043468db58ac62a92d002b6" format="dita" scope="local">事件回呼</a> 。 </p> </li> 
      <li id="li_FE5B330E98834CB08C16FCA694F31BE3"> <p> <span class="codeph"> 本地化 </span> 的文本 — {  <span class="codeph"> Object  </span>} JSON對象，包含本地化資料。選填。 </p> <p>如需詳細資訊，請參閱<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74" format="dita" scope="local">使用者介面元素的本地化</a> 。 </p> <p>如需物件內容的詳細資訊，另請參閱<i>檢視器SDK使用指南</i>和範例。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 傳回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

無。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
var eCatalogViewer = new s7viewers.eCatalogViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/Pluralist", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
}, 
"handlers":{ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
}, 
"localizedTexts":{ 
"en":{ 
"CloseButton.TOOLTIP":"Close" 
}, 
"fr":{ 
"CloseButton.TOOLTIP":"Fermer" 
}, 
defaultLocale:"en" 
} 
});
```
