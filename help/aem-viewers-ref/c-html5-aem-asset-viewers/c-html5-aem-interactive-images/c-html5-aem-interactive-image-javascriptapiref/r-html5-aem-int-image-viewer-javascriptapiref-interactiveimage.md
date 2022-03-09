---
title: 互動式影像
description: 視頻影像查看器的JavaScript API參考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 165de14f-0031-4969-9671-5da310d44c28
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 3%

---

# 互動式影像{#interactiveimage}

視頻影像查看器的JavaScript API參考。

`InteractiveImage([config])`

建構子，建立視頻影像查看器實例。

## 參數 {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 配置 </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {object} </span> 可選JSON配置對象，允許所有查看器設定傳遞到建構子以避免調用單個setter方法。 包含以下屬性： </p> <p> 
     <ul id="ul_789DBD5B72ED4C80B685455B0D59494D"> 
      <li id="li_28FDCB53E4AD4097A51F21B876C18FB1"> <p> <span class="codeph"> 容器ID </span> - <span class="codeph"> {字串} </span> DOM容器的ID(通常為 <span class="codeph"> DIV </span>)。 調用此方法時，不必建立容器元素。 但是，當 <span class="codeph"> init() </span> 。 </p> <p>必要. </p> </li> 
      <li id="li_FDE00392DC1544ABBDD75F81EF814EF2"> <p> <span class="codeph"> 帕拉 </span> - <span class="codeph"> {對象} </span> JSON對象，其中屬性名稱是特定於查看器的配置選項或SDK修飾符，並且該屬性的值是相應的設定值。 </p> <p>必要. </p> </li> 
      <li id="li_C534D5091CDA4717BCC48E3EBBF09AB8"> <p> <span class="codeph"> 處理程式 </span> - <span class="codeph"> {對象} </span> 具有查看器事件回調的JSON對象，其中屬性名稱是支援的查看器事件的名稱，屬性值是對相應回調的JavaScript函式引用。 </p> <p>選填。 </p> <p>請參閱 <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-event-callbacks.md#concept-66d5996f2b1b44cab3d5264cda5c50cd" format="dita" scope="local"> 事件回調 </a> 的子菜單。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 返回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

無。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```javascript {.line-numbers}
var interactiveImage = new s7viewers.InteractiveImage({ 
 "containerId":"s7viewer", 
 "params":{ 
  "asset":"/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg", 
  "serverurl":"http://aodmarketingna.assetsadobe.com/is/image" 
}, 
"handlers":{ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
} 
});
```
