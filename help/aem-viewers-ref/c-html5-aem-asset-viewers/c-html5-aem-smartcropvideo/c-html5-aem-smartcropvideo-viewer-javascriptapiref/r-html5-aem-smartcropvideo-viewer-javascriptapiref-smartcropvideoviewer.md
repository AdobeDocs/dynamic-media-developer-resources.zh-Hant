---
title: SmartCropVideoViewer
description: 用於Smart Crop Video Viewer的JavaScript API參考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 55885e57-4a21-43bb-86b0-9ac34bd29bd0
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 3%

---

# SmartCropVideoViewer{#smartcropvideoviewer}

用於Smart Crop Video Viewer的JavaScript API參考。

`SmartCropVideoViewer([config])`

建構子；建立Smart Crop Video Viewer實例。

## 參數 {#section-8bc3d1424c8444f193716fc8d9975765}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 配置 </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {對象} </span> 可選的JSON配置對象，允許所有查看器設定傳遞到建構子，並避免調用單個setter方法。 包含以下屬性： </p> <p> 
     <ul id="ul_266C711E8E75471E90C15F39A96A142F"> 
      <li id="li_71857BBD652243A094E936C2C8EA9702"> <span class="codeph"> 容器ID </span> - <span class="codeph"> {字串} </span> DOM容器的ID(通常為 <span class="codeph"> DIV </span>)。 不必在調用此方法時建立容器元素。 但是，當 <span class="codeph"> init() </span> 。 必要. </li> 
      <li id="li_3D28979F04274AC9B507B33D4275FC3A"> <span class="codeph"> 帕拉 </span> - <span class="codeph"> {對象} </span> JSON對象，其中屬性名稱是特定於查看器的配置選項或SDK修飾符，並且該屬性的值是相應的設定值。 必要. </li> 
      <li id="li_A40AC2167575415FB3383D070E27B9AB"> <span class="codeph"> 處理程式 </span> - <span class="codeph"> {對象} </span> 具有查看器事件回調的JSON對象，其中屬性名稱是支援的查看器事件的名稱，屬性值是對相應回調的JavaScript函式引用。 選擇性. <p>請參閱 <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-event-callbacks.md#concept-ebe5a4c1853d4912a919d86df35c1f6d" format="dita" scope="local"> 事件回調 </a> 的子菜單。 </p> </li> 
      <li id="li_D344288C9B584E569F7BF92D960F9DF8"> <p> <span class="codeph"> 本地化文本 </span> - { <span class="codeph"> 對象 </span>}包含本地化資料的JSON對象。 選擇性. </p> <p>請參閱 <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-namespace.md#concept-679bfabb3e3e4c12a285c4e9c4144153" format="dita" scope="local"> 查看器SDK命名空間 </a> 的子菜單。 </p> <p>查看 <i>查看器SDK使用手冊</i> 以及有關對象內容的詳細資訊的示例。 選擇性. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 返回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

無。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```javascript {.line-numbers}
var smartCropVideoViewer = new s7viewers.SmartCropVideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Glacier_Climber_MP4", 
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
"SmartCropVideoPlayer.ERROR":"Your Browser does not support HTML5 Video tag or the video cannot be played." 
}, 
"fr":{ 
"SmartCropVideoPlayer.ERROR":"Votre navigateur ne prend pas en charge la vidéo HTML5 tag ou la vidéo ne peuvent pas être lus." 
}, 
defaultLocale:"en" 
} 
});
```
