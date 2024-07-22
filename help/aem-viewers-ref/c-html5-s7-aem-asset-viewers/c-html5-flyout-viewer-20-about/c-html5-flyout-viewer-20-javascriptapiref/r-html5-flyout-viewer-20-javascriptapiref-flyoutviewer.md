---
title: 彈出式檢視器
description: 彈出式檢視器的JavaScript API參考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: b64f16c8-03bf-4603-972f-845a4c1e2b02
source-git-commit: f970421ccc482b698343aa18e7dfde7bea4c2a89
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 3%

---

# 彈出式檢視器{#flyoutviewer}

彈出式檢視器的JavaScript API參考。

`FlyoutViewer([config])`

建構函式；建立彈出式檢視器例項。

## 參數 {#section-8bc3d1424c8444f193716fc8d9975765}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">設定</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object} </span>選用的JSON組態物件，允許所有檢視器設定傳遞給建構函式，並避免呼叫個別setter方法。 包含下列屬性： </p> <p> 
     <ul id="ul_266C711E8E75471E90C15F39A96A142F"> 
      <li id="li_71857BBD652243A094E936C2C8EA9702"> 檢視器插入的DOM容器的<span class="codeph"> containerId </span> - <span class="codeph"> {String} </span> ID （通常是<span class="codeph"> DIV </span>）。 不需要在呼叫此方法時建立容器元素。 不過，執行<span class="codeph"> init() </span>時，容器必須存在。 必要. </li> 
      <li id="li_3D28979F04274AC9B507B33D4275FC3A"> <span class="codeph">引數</span> - <span class="codeph"> {Object} </span> JSON物件搭配檢視器組態引數，其中屬性名稱是檢視器特定的組態選項或SDK修飾元，且該屬性的值是對應的設定值。 必要. </li> 
      <li id="li_A40AC2167575415FB3383D070E27B9AB"> <span class="codeph">處理常式</span> - <span class="codeph"> {Object} </span>具有檢視器事件回呼的JSON物件，其中屬性名稱是支援的檢視器事件的名稱，屬性值是適當回呼的JavaScript函式參考。 選擇性. <p>如需檢視器事件的詳細資訊，請參閱<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-event-callbacks.md#concept-53eb01d28189437790268da4929f2a10" format="dita" scope="local">事件回呼</a>。 </p> </li> 
      <li id="li_218F9597A60249AEBA43A9E86EAFF8BA"> <p> <span class="codeph"> localizedTexts </span> - { <span class="codeph">物件</span>} JSON物件包含本地化資料。 選擇性. </p> <p>如需詳細資訊，請參閱<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27" format="dita" scope="local">使用者介面元素</a>的本地化。 </p> <p>如需物件內容的詳細資訊，請參閱<i>檢視器SDK使用手冊</i>和範例。 選擇性. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 傳回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

無。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```javascript {.line-numbers}
var flyoutViewer = new s7viewers.FlyoutViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
}, 
"handlers":{ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
}, 
"localizedTexts":{ 
"en":{ 
"FlyoutZoomView.TIP_BUBBLE_OVER":"Mouse over to zoom" 
}, 
"fr":{ 
"FlyoutZoomView.TIP_BUBBLE_OVER":"Passez la souris sur pour zoomer" 
}, 
defaultLocale:"en" 
} 
});
```
