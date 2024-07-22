---
title: 基本縮放檢視器
description: 基本縮放檢視器的JavaScript API參考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 320f740e-c6b9-44d6-9369-9c2ec31189c5
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 3%

---

# 基本縮放檢視器{#basiczoomviewer}

基本縮放檢視器的JavaScript API參考。

`BasicZoomViewer([config])`

建構函式，建立基本縮放檢視器實體。

## 參數 {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">設定</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {object} </span>選用的JSON組態物件，允許所有檢視器設定傳遞至建構函式，以避免呼叫個別setter方法。 包含下列屬性： </p> <p> 
     <ul id="ul_789DBD5B72ED4C80B685455B0D59494D"> 
      <li id="li_28FDCB53E4AD4097A51F21B876C18FB1"> <p> 檢視器插入的DOM容器的<span class="codeph"> containerId </span> - <span class="codeph"> {String} </span> ID （通常是<span class="codeph"> DIV </span>）。 呼叫此方法時，不需要建立容器元素。 不過，執行<span class="codeph"> init() </span>時，容器必須存在。 必要. </p> </li> 
      <li id="li_FDE00392DC1544ABBDD75F81EF814EF2"> <p> <span class="codeph">引數</span> - <span class="codeph"> {Object} </span> JSON物件搭配檢視器組態引數，其中屬性名稱為檢視器特定組態選項或SDK修飾元，且該屬性的值為對應的設定值。 必要. </p> </li> 
      <li id="li_C534D5091CDA4717BCC48E3EBBF09AB8"> <p> <span class="codeph">處理常式</span> - <span class="codeph"> {Object} </span>具有檢視器事件回呼的JSON物件，其中屬性名稱是支援的檢視器事件的名稱，而屬性值是適當回呼的JavaScript函式參考。 選擇性. </p> <p>如需檢視器事件的詳細資訊，請參閱<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-event-callbacks.md#concept-8ba57cf86537401999514e1b221ec734" format="dita" scope="local">事件回呼</a>。 </p> </li> 
      <li id="li_528FE03845F847E08F964E38D6AB6E86"> <p> <span class="codeph"> localizedTexts </span> - <span class="codeph"> {Object} </span> JSON物件包含本地化資料。 選擇性. </p> <p>如需詳細資訊，請參閱<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74" format="dita" scope="local">使用者介面元素</a>的本地化。 </p> <p> 另請參閱<i>檢視器SDK使用手冊</i>和範例，以取得物件內容的詳細資訊。 選擇性 </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 傳回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

無。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```javascript {.line-numbers}
var basicZoomViewer = new s7viewers.BasicZoomViewer({ 
 "containerId":"s7viewer", 
 "params":{ 
  "asset":"Scene7SharedAssets/Backpack_B", 
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
