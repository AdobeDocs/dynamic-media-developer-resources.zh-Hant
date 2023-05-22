---
title: getComponent
description: 視頻影像查看器的JavaScript API參考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 5f2514a9-bbd0-436d-ad96-b89778604f8a
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 1%

---

# getComponent{#getcomponent}

視頻影像查看器的JavaScript API參考。

`getComponent(componentId)`

返回對查看器使用的Viewer SDK元件的引用。 該網頁可以使用這種方法來擴展或定制出廠時查看器的行為。 僅在 `initComplete` 查看器回調已運行，否則查看器邏輯可能尚未建立元件。

## 參數 {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

`*`元件ID`*` - `{String}` 查看器使用的查看器SDK元件的ID。 此查看器支援以下元件ID:

<table id="table_7B5DD9303EF44ADD847B13FFEAD135D9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>元件ID </p> </th> 
   <th colname="col2" class="entry"> <p>查看器SDK元件類名 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 參數管理器 </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.ParameterManager </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 容器 </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.container </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 媒體集 </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.MediaSet </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 縮放視圖 </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.image.ZoomView </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imageMapEffect </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.image.mageMapEffect </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

使用SDK API時，必須使用正確的完全限定的SDK命名空間，如中所述 [查看器SDK命名空間](../../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-namespace.md#concept-00a31b9bc7eb4014b28c1ba661fe5265)。

有關特定元件的詳細資訊，請參閱查看器SDK API文檔。

## 返回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` 對查看器SDK元件的引用。 方法返回 `null` 的 `componentId` 不是受支援的查看器元件，或者如果查看器邏輯尚未建立該元件。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var zoomView = <instance>.getComponent("zoomView"); 
} 
})
```
