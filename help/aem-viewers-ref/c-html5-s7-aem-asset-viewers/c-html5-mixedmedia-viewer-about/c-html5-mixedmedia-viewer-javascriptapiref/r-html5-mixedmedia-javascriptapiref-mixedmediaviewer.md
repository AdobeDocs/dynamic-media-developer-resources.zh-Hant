---
description: 混合媒體檢視器的JavaScript API參考。
solution: Experience Manager
title: MixedMediaViewer
feature: Dynamic Media Classic,Viewers,SDK/API,Mix Media Sets
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 3%

---


# MixedMediaViewer{#mixedmediaviewer}

混合媒體檢視器的JavaScript API參考。

`MixedMediaViewer([config])`

建構函式，會建立新的混合媒體檢視器例項。

## 參數 {#section-8bc3d1424c8444f193716fc8d9975765}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> config  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object}可選 </span> 的JSON設定物件，可讓所有檢視器設定傳遞至建構函式，並避免呼叫個別的setter方法。包含下列屬性： </p> <p> 
     <ul id="ul_266C711E8E75471E90C15F39A96A142F"> 
      <li id="li_71857BBD652243A094E936C2C8EA9702"> <span class="codeph"> containerId  </span> -  <span class="codeph"> {String}  </span> ID檢視器所插入之DOM容器(通常 <span class="codeph"> 是 </span>DIV)。您不需要在呼叫此方法時建立容器元素。 但是，當<span class="codeph"> init()</span>運行時，容器必須存在。 必要. </li> 
      <li id="li_3D28979F04274AC9B507B33D4275FC3A"> <span class="codeph"> params  </span> -  <span class="codeph"> {Object}  </span> JSON物件與檢視器設定參數，其中屬性名稱為檢視器專用的設定選項或SDK修飾元，且該屬性的值為對應的設定值。必要. </li> 
      <li id="li_A40AC2167575415FB3383D070E27B9AB"> <span class="codeph"> 處理 </span> 常式-  <span class="codeph"> {Object}  </span> JSON物件與檢視器事件回呼，其中屬性名稱是支援之檢視器事件的名稱，屬性值是適當回呼的JavaScript函式參考。選填。 <p>如需檢視器事件的詳細資訊，請參閱<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-event-callbacks.md#concept-273d2cddbb7144e284b618ffaf3deabc" format="dita" scope="local">事件回呼</a>。 </p> </li> 
      <li id="li_C592026403804A4FAE12863944A10EE4"> <p> <span class="codeph"> localizedTexts  </span> - {  <span class="codeph"> Object </span>} JSON物件與本地化資料。選填。 </p> <p>如需詳細資訊，請參閱<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-localization.md#concept-16262b8096474d6c9c018c3e99110dd1" format="dita" scope="local">使用者介面元素的本地化。</a> </p> <p>另請參閱<i>檢視器SDK使用指南</i>和範例，以取得有關物件內容的詳細資訊。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 傳回{#section-1d3cf85bc7cc4dfe9670e038d02b9101}

無。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
var mixedMediaViewer = new s7viewers.MixedMediaViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Mixed_Media_Set_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
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

