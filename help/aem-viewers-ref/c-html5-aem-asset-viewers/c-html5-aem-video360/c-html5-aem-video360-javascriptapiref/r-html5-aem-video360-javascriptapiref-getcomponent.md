---
description: Video360檢視器的JavaScript API參考。
solution: Experience Manager
title: getComponent
feature: Dynamic Media Classic，檢視器，SDK/API,360 VR影片
role: Developer,User
exl-id: bc5f0046-8e20-4ff0-a90f-05c38f686ad2
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 1%

---

# getComponent{#getcomponent}

Video360檢視器的JavaScript API參考。

`getComponent(componentId)`

傳回檢視器所使用之檢視器SDK元件的參考。 網頁可使用此方法來擴充或自訂現成檢視器的行為。 只有在`initComplete`檢視器回呼執行後才呼叫此方法，否則檢視器邏輯可能尚未建立元件。

## 參數 {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

`*`componentID`*`  — 檢 `{String}` 視器使用之檢視器SDK元件的ID。此檢視器支援下列元件ID:

<table id="table_7B5DD9303EF44ADD847B13FFEAD135D9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>元件ID </p> </th> 
   <th colname="col2" class="entry"> <p>檢視器SDK元件類別名稱 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> parameterManager  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.ParameterManager  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 容器 </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.container  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mediaSet  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.MediaSet  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> video360Player  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.video.Video360Player  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> fullScreenButton  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.FullScreenButton  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mutableVolume  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.video.MutableVolume  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> playPauseButton  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.PlayPauseButton  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> videoScrubber  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.video.VideoScrubber  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> videoTime  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.video.VideoTime  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 控制項 </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.ControlBar  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> socialShare  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.share.SocialShare  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> twitterShare  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.share.TwitterShare  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> facebookShare  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.share.FacebookShare  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> linkShare  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.share.LinkShare  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> embedShare  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sk.share.EmbedShare  </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

使用SDK API時，請務必依照[檢視器SDK命名空間](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-viewer-sdk-namespace.md#concept-4ee8657c7d67421f8e7880130a246621)中所述，使用正確的完全限定SDK命名空間。

如需特定元件的詳細資訊，請參閱&#x200B;*HTML5檢視器SDK API*&#x200B;檔案。

## 傳回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` 檢視器SDK元件的參考。如果`componentId`不是支援的檢視器元件，或檢視器邏輯尚未建立元件，則方法會傳回`null`。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var video360Player = <instance>.getComponent("video360Player"); 
} 
})
```
