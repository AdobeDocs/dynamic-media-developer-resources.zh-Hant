---
title: setHandlers
description: Carousel查看器的JavaScript API參考
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: d269627a-e2f8-4ca6-96a1-a7dce312e06e
source-git-commit: 96ac67e5645c2c55920cc971806ba2f14ae57044
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 3%

---

# setHandlers{#sethandlers}

Carousel查看器的JavaScript API參考

`setHandlers(handlers)`

指定零個或多個回調處理程式。 對此方法的調用將完全覆蓋以前為該查看器實例分配的事件處理程式。 必須在之前調用 `init()`。

## 參數 {#section-b60f082cca1542748b605689b1d43f8a}

<table id="table_98A620DAE2C340FA97BF7204AE023CC8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 處理程式 </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {對象} </span> 具有查看器事件回調的JSON對象。 屬性名稱是支援的查看器事件的名稱。 屬性值是對相應回調的JavaScript函式引用。 </p> <p>請參閱 <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-event-callbacks.md#concept-66d5996f2b1b44cab3d5264cda5c50cd" format="dita" scope="local"> 事件回調 </a> 的子菜單。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 返回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

無。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
})
```
