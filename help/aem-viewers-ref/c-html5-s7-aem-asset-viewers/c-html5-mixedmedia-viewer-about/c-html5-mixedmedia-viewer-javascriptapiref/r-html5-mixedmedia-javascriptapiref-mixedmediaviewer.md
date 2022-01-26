---
title: MixedMediaViewer
description: 用於混合媒體查看器的JavaScript API參考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: b7f09f51-409e-4dfa-9041-b82767d4e35f
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 3%

---

# MixedMediaViewer{#mixedmediaviewer}

用於混合媒體查看器的JavaScript API參考。

`MixedMediaViewer([config])`

建構子，建立新的混合媒體查看器實例。

## 參數 {#section-8bc3d1424c8444f193716fc8d9975765}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 配置 </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {對象} </span> 可選的JSON配置對象，允許所有查看器設定傳遞到建構子，並避免調用單個setter方法。 包含以下屬性： </p> <p> 
     <ul id="ul_266C711E8E75471E90C15F39A96A142F"> 
      <li id="li_71857BBD652243A094E936C2C8EA9702"> <span class="codeph"> 容器ID </span> - <span class="codeph"> {字串} </span> DOM容器的ID(通常為 <span class="codeph"> DIV </span>)。 不必在調用此方法時建立容器元素。 但是，當 <span class="codeph"> init() </span> 。 必要. </li> 
      <li id="li_3D28979F04274AC9B507B33D4275FC3A"> <span class="codeph"> 帕拉 </span> - <span class="codeph"> {對象} </span> JSON對象，其中屬性名稱是特定於查看器的配置選項或SDK修飾符，並且該屬性的值是相應的設定值。 必要. </li> 
      <li id="li_A40AC2167575415FB3383D070E27B9AB"> <span class="codeph"> 處理程式 </span> - <span class="codeph"> {對象} </span> 具有查看器事件回調的JSON對象，其中屬性名稱是支援的查看器事件的名稱，屬性值是對相應回調的JavaScript函式引用。 選填。 <p>請參閱 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-event-callbacks.md#concept-273d2cddbb7144e284b618ffaf3deabc" format="dita" scope="local"> 事件回調 </a> 的子菜單。 </p> </li> 
      <li id="li_C592026403804A4FAE12863944A10EE4"> <p> <span class="codeph"> 本地化文本 </span> - { <span class="codeph"> 對象 </span>}包含本地化資料的JSON對象。 選填。 </p> <p>請參閱 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-localization.md#concept-16262b8096474d6c9c018c3e99110dd1" format="dita" scope="local"> 用戶介面元素的本地化 </a> 的子菜單。 </p> <p>另請參閱 <i>查看器SDK使用手冊</i> 以及有關對象內容的詳細資訊的示例。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 返回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

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
