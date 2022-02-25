---
title: getComponent
description: 用於基本縮放查看器的JavaScript API參考
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: e9bf641f-5bc9-42d9-a030-5591cd883373
source-git-commit: 61e3a1fd0e21d336eaf5232096f5b1b54f2a6353
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 1%

---

# getComponent{#getcomponent}

用於基本縮放查看器的JavaScript API參考

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
   <td colname="col1"> <p> <span class="codeph"> 縮放InButton </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.ZoomInButton </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 縮小按鈕 </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.ZoomOutButton </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomResetButton </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.ZoomResetButton </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 全屏按鈕 </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.FullScreenButton </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> closeButton </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.CloseButton </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

使用SDK API時，必須使用正確、完全限定的SDK命名空間，如Viewer SDK命名空間中所述

有關特定元件的詳細資訊，請參閱查看器SDK API文檔。

## 返回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

的 `{Object}` 是對查看器SDK元件的引用。 方法返回 `null` 的 `componentId` 不是受支援的查看器元件，或者如果查看器邏輯尚未建立該元件。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var zoomView = <instance>.getComponent("zoomView"); 
} 
})
```
