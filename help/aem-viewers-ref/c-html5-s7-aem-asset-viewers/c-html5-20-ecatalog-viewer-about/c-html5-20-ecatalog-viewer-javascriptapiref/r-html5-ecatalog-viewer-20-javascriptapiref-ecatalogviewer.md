---
title: eCatalogViewer
description: eCatalog Viewer的JavaScript API參考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 111699a3-8a70-4caf-b7da-7b594b785f7c
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 3%

---

# eCatalogViewer{#ecatalogviewer}

eCatalog Viewer的JavaScript API參考。

`eCatalogViewer([config])`

建構子，建立eCatalog查看器實例。

## 參數 {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 配置 </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {對象} </span> 可選的JSON配置對象，允許所有查看器設定傳遞到建構子，並避免調用單個setter方法。 包含以下屬性： </p> <p> 
     <ul id="ul_266C711E8E75471E90C15F39A96A142F"> 
      <li id="li_71857BBD652243A094E936C2C8EA9702"> <p> <span class="codeph"> 容器ID </span> - <span class="codeph"> {字串} </span> DOM容器的ID(通常為 <span class="codeph"> DIV </span>)。 不必在調用此方法時建立容器元素。 但是，當 <span class="codeph"> init() </span> 。 必要. </p> </li> 
      <li id="li_3D28979F04274AC9B507B33D4275FC3A"> <p> <span class="codeph"> 帕拉 </span> - <span class="codeph"> {對象} </span> JSON對象，其中屬性名稱是特定於查看器的配置選項或SDK修飾符，並且該屬性的值是相應的設定值。 必要. </p> </li> 
      <li id="li_A40AC2167575415FB3383D070E27B9AB"> <p> <span class="codeph"> 處理程式 </span> - <span class="codeph"> {對象} </span> 具有查看器事件回調的JSON對象，其中屬性名稱是支援的查看器事件的名稱，屬性值是對相應回調的JavaScript函式引用。 選填。 </p> <p>請參閱 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-event-callbacks.md#concept-0bf5ff877043468db58ac62a92d002b6" format="dita" scope="local"> 事件回調 </a> 的子菜單。 </p> </li> 
      <li id="li_FE5B330E98834CB08C16FCA694F31BE3"> <p> <span class="codeph"> 本地化文本 </span> - { <span class="codeph"> 對象 </span>}包含本地化資料的JSON對象。 選填。 </p> <p>請參閱 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74" format="dita" scope="local"> 用戶介面元素的本地化 </a> 的子菜單。 </p> <p>另請參閱 <i>查看器SDK使用手冊</i> 以及有關對象內容的詳細資訊的示例。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 返回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

無。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```javascript {.line-numbers}
var eCatalogViewer = new s7viewers.eCatalogViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/Pluralist", 
 "serverurl":"https://s7d1.scene7.com/is/image/" 
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
