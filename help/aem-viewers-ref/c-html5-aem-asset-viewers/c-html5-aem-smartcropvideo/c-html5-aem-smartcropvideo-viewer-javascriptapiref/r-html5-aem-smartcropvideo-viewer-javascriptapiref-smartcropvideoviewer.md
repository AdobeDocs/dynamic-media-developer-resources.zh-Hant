---
title: SmartCropVideoViewer
description: 智慧型裁切視訊檢視器的JavaScript API參考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: null
source-git-commit: 254d1ef05c73e19618b7ad4743c6a242fa177929
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 3%

---

# SmartCropVideoViewer{#smartcropvideoviewer}

智慧型裁切視訊檢視器的JavaScript API參考。

`SmartCropVideoViewer([config])`

建構子；會建立智慧型裁切視訊檢視器例項。

## 參數 {#section-8bc3d1424c8444f193716fc8d9975765}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 設定 </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {對象} </span> 選用的JSON設定物件，可讓所有檢視器設定傳遞至建構函式，並避免呼叫個別setter方法。 包含下列屬性： </p> <p> 
     <ul id="ul_266C711E8E75471E90C15F39A96A142F"> 
      <li id="li_71857BBD652243A094E936C2C8EA9702"> <span class="codeph"> containerId </span> - <span class="codeph"> {String} </span> DOM容器的ID(通常為 <span class="codeph"> DIV </span>)，檢視器即會插入。 呼叫此方法時，不需要建立容器元素。 然而，容器必須存在於 <span class="codeph"> init() </span> 執行中。 必要. </li> 
      <li id="li_3D28979F04274AC9B507B33D4275FC3A"> <span class="codeph"> params </span> - <span class="codeph"> {對象} </span> JSON物件，其檢視器設定參數中的屬性名稱為檢視器專屬的設定選項或SDK修飾元，而該屬性的值為對應的設定值。 必要. </li> 
      <li id="li_A40AC2167575415FB3383D070E27B9AB"> <span class="codeph"> 處理器 </span> - <span class="codeph"> {對象} </span> 具有檢視器事件回呼的JSON物件，其中屬性名稱是支援的檢視器事件名稱，而屬性值是適當回呼的JavaScript函式參考。 選填。 <p>請參閱 <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-event-callbacks.md#concept-ebe5a4c1853d4912a919d86df35c1f6d" format="dita" scope="local"> 事件回呼 </a> 以取得檢視器事件的詳細資訊。 </p> </li> 
      <li id="li_D344288C9B584E569F7BF92D960F9DF8"> <p> <span class="codeph"> localizedTexts </span> - { <span class="codeph"> 物件 </span>}含有本地化資料的JSON物件。 選填。 </p> <p>請參閱 <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-namespace.md#concept-679bfabb3e3e4c12a285c4e9c4144153" format="dita" scope="local"> 檢視器SDK命名空間 </a> 以取得更多資訊。 </p> <p>請參閱 <i>檢視器SDK使用手冊</i> 和範例，以取得物件內容的詳細資訊。 選填。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 傳回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

無。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
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
