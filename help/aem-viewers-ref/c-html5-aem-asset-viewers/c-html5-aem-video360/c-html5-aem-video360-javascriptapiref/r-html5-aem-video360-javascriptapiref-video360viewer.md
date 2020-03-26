---
description: Video360檢視器的JavaScript API參考。
seo-description: Video360檢視器的JavaScript API參考。
seo-title: Video360Viewer
solution: Experience Manager
title: Video360Viewer
topic: Dynamic media
uuid: b5d5e270-687c-40aa-9de4-c5bc2a7806f7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Video360Viewer{#video-viewer}

Video360檢視器的JavaScript API參考。

`Video360Viewer([config])`

建構函式，會建立新的HTML5 Video360檢視器例項。

## 參數 {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 配置 </span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {object}可 </span> 選的JSON設定物件，可讓所有檢視器設定傳遞至建構函式，以避免呼叫個別的setter方法。 包含下列屬性： </p> <p> 
     <ul id="ul_789DBD5B72ED4C80B685455B0D59494D"> 
      <li id="li_28FDCB53E4AD4097A51F21B876C18FB1"> <p> <span class="codeph"> containerId </span> - <span class="codeph"> {String} </span> ID的DOM容器(通常是 <span class="codeph"> DIV </span>)，檢視器會插入其中。 呼叫此方法時，不需要建立容器元素。 但是，執行init()時 <span class="codeph"> 必須存 </span> 在容器。 </p> <p>必要. </p> </li> 
      <li id="li_FDE00392DC1544ABBDD75F81EF814EF2"> <p> <span class="codeph"> params </span> - <span class="codeph"> {Object} </span> JSON物件與檢視器設定參數，其中屬性名稱為檢視器專用的設定選項或SDK修飾元，且該屬性的值是對應的設定值。 </p> <p>必要. </p> </li> 
      <li id="li_C534D5091CDA4717BCC48E3EBBF09AB8"> <p> <span class="codeph"> 處理 </span> 程式- <span class="codeph"> {Object} </span> JSON物件與檢視器事件回呼，其中屬性名稱是支援之檢視器事件的名稱，屬性值是適當回呼的JavaScript函式參考。 </p> <p>選填。 </p> <p>如需檢 <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-event-callbacks.md#concept-66d5996f2b1b44cab3d5264cda5c50cd" format="dita" scope="local"> 視器事件 </a> 的詳細資訊，請參閱事件回呼。 </p> </li> 
      <li id="li_42A3F3BEF1004E069F0FB2AE0A30B093"> <p> <span class="codeph"> localizedTexts </span> - <span class="codeph"> {Object} </span> JSON物件與本地化資料。 選填。 </p> <p>如需詳 <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1" format="dita" scope="local"> 細資訊，請參閱使用者介面元 </a> 素的本地化。 </p> <p>另請參閱檢 <i>視器SDK使用指南</i> ，以及範例，以取得物件內容的詳細資訊。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

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

