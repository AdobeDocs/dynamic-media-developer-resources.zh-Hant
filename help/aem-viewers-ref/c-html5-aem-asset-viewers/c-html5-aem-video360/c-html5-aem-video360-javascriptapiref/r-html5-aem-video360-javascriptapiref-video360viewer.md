---
description: Video360檢視器的JavaScript API參考。
solution: Experience Manager
title: Video360Viewer
feature: Dynamic Media Classic，檢視器，SDK/API,360 VR影片
role: Developer,Business Practitioner
exl-id: ab22ff22-45a7-490e-932d-7c885ff5c3a9
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 5%

---

# Video360Viewer{#video-viewer}

Video360檢視器的JavaScript API參考。

`Video360Viewer([config])`

建構函式會建立新的HTML5 Video360檢視器例項。

## 參數 {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 設定  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {object}選 </span> 用的JSON配置對象允許所有查看器設定傳遞給建構子，以避免調用單個setter方法。包含下列屬性： </p> <p> 
     <ul id="ul_789DBD5B72ED4C80B685455B0D59494D"> 
      <li id="li_28FDCB53E4AD4097A51F21B876C18FB1"> <p> <span class="codeph"> containerId  </span> -  <span class="codeph"> {String}  </span> DOM容器的ID(通常是 <span class="codeph"> DIV </span>)，會將檢視器插入其中。呼叫此方法時，不需要建立容器元素。 但是，當<span class="codeph"> init()</span>運行時，容器必須存在。 </p> <p>必要. </p> </li> 
      <li id="li_FDE00392DC1544ABBDD75F81EF814EF2"> <p> <span class="codeph"> 參 </span> 數 —  <span class="codeph"> {Object} JSON </span> 物件以及檢視器設定參數，其中屬性名稱為檢視器專屬組態選項或SDK修飾元，而該屬性的值是對應的設定值。 </p> <p>必要. </p> </li> 
      <li id="li_C534D5091CDA4717BCC48E3EBBF09AB8"> <p> <span class="codeph"> 處理 </span> 程式 —  <span class="codeph"> {Object} JSON物 </span> 件，具有檢視器事件回呼，其中屬性名稱是受支援檢視器事件的名稱，而屬性值是適當回呼的JavaScript函式參考。 </p> <p>選填。 </p> <p>如需檢視器事件的詳細資訊，請參閱<a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-event-callbacks.md#concept-66d5996f2b1b44cab3d5264cda5c50cd" format="dita" scope="local">事件回呼</a> 。 </p> </li> 
      <li id="li_42A3F3BEF1004E069F0FB2AE0A30B093"> <p> <span class="codeph"> 本地化 </span> 文本 —  <span class="codeph"> {Object} JSON </span> 物件，包含本地化資料。選填。 </p> <p>如需詳細資訊，請參閱<a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1" format="dita" scope="local">使用者介面元素的本地化</a> 。 </p> <p>如需物件內容的詳細資訊，另請參閱<i>檢視器SDK使用指南</i>和範例。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 傳回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

無。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
var video360Viewer = new s7viewers.Video360Viewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/space_station_360-AVS", 
 "serverurl":"https://s7d9.scene7.com/is/image/", 
 "videoserverurl":"https://s7d9.scene7.com/is/content/" 
}, 
"handlers":{ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
}, 
"localizedTexts":{ 
"en":{ 
"Video360Player.ERROR":"Your Browser does not support HTML5 Video tag or the video cannot be played." 
}, 
"fr":{ 
"Video360Player.ERROR":"Votre navigateur ne prend pas en charge la vidéo HTML5 tag ou la vidéo ne peuvent pas être lus." 
}, 
defaultLocale:"en" 
} 
});
```
