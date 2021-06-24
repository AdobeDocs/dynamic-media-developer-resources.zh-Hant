---
description: 輪播檢視器的JavaScript API參考。
solution: Experience Manager
title: 轉盤檢視器
feature: Dynamic Media Classic，檢視器，SDK/API，輪播橫幅
role: Developer,Business Practitioner
exl-id: 890d869d-dbf2-4c24-88d1-34c439ab1e3a
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 3%

---

# 轉盤檢視器{#carouselviewer}

輪播檢視器的JavaScript API參考。

`CarouselViewer([config])`

建構函式會建立新的HTML 5輪播檢視器例項。

## 參數 {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 設定  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {object}選 </span> 用的JSON配置對象允許所有查看器設定傳遞給建構子，以避免調用單個setter方法。包含下列屬性： </p> <p> 
     <ul id="ul_789DBD5B72ED4C80B685455B0D59494D"> 
      <li id="li_28FDCB53E4AD4097A51F21B876C18FB1"> <p> <span class="codeph"> containerId  </span> -  <span class="codeph"> { </span> String} DOM容器(通常是 <span class="codeph"> DIV </span>)的ID。呼叫此方法時，不需要建立容器元素。 但是，當<span class="codeph"> init()</span>運行時，容器必須存在。 </p> <p>必要. </p> </li> 
      <li id="li_FDE00392DC1544ABBDD75F81EF814EF2"> <p> <span class="codeph"> 參 </span> 數 —  <span class="codeph"> {Object} JSON </span> 物件以及檢視器設定參數，其中屬性名稱為檢視器專屬組態選項或SDK修飾元，而該屬性的值是對應的設定值。 </p> <p>必要. </p> </li> 
      <li id="li_C534D5091CDA4717BCC48E3EBBF09AB8"> <p> <span class="codeph"> 處理 </span> 程式 —  <span class="codeph"> {Object} JSON物 </span> 件，具有檢視器事件回呼，其中屬性名稱是受支援檢視器事件的名稱，而屬性值是適當回呼的JavaScript函式參考。 </p> <p>選填。 </p> <p>如需檢視器事件的詳細資訊，請參閱<a href="../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-event-callbacks.md#concept-66d5996f2b1b44cab3d5264cda5c50cd" format="dita" scope="local">事件回呼</a> 。 </p> </li> 
      <li id="li_CD88EDB586B241DBB87B13709F24C454"> <p> <span class="codeph"> localizedTexts  </span> -  <span class="codeph"> {Object}  </span> </p> <p> 含有本地化資料的JSON物件。 如需物件內容的詳細資訊，請參閱使用者介面元素本地化和範例。 </p> <p>選擇性 </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 傳回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

無。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
var carouselViewer = new s7viewers.CarouselViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner", 
 "serverurl":"https://adobedemo62-h.assetsadobe.com/is/image" 
}, 
"handlers":{ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
}, 
"localizedTexts":{ 
"en":{ 
"PanLeftButton.TOOLTIP":"Left" 
}, 
"fr":{ 
"PanLeftButton.TOOLTIP":"Gauchiste" 
}, 
defaultLocale:"en" 
} 
});
```
