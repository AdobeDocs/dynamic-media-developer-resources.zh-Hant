---
description: 混合媒體檢視器的JavaScript API參考。
solution: Experience Manager
title: setAsset
feature: Dynamic Media Classic，檢視器，SDK/API，混合媒體集
role: Developer,Business Practitioner
exl-id: 3ad78de9-17a6-40c9-b389-a1f7eed11635
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 1%

---

# setAsset{#setasset}

混合媒體檢視器的JavaScript API參考。

` setAsset( *`asset`*[,data]))`

設定新資產和選用的其他資產資料。 您可以在`init()`之前或之後隨時呼叫此參數。 如果在`init()`之後呼叫，檢視器會在執行階段交換資產。

另請參閱[init](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-javascriptapiref/r-html5-mixedmedia-javascriptapiref-init.md#reference-bb4428c155e541b79797f96e17c068ae)。

## 參數 {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

`*`asset`*`  - {  `String`}個新資產ID或明確的混合媒體集，之後附加選用的「影像伺服」修飾元 `?`。

此檢視器不支援使用IR（影像轉譯）或UGC（使用者產生的內容）的影像。

`*`資料`*`  - {  `JSON`}新字幕檔案的位置。

如果未指定，則註解按鈕在用戶介面中不可見。 使用此參數指定的字幕適用於混合媒體集中最先出現的視頻；後續視頻播放沒有字幕。 此檢視器支援下列元件ID:

<table id="table_7B5DD9303EF44ADD847B13FFEAD135D9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>元件ID </p> </th> 
   <th colname="col2" class="entry"> <p>檢視器SDK元件類別名稱 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 後驗影像  </span> </p> </td> 
   <td colname="col2"> <p>在視訊開始播放之前，要在第一個影格上顯示的影像。 </p> <p>請參閱<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/r-html5-mixedmedia-viewer-config-attrib/r-html5-mixedmedia-viewer-config-attrib-videoplayer-posterimage.md#reference-f424ad0f278b4d14b86ea55e3a73c52b" format="dita" scope="local"> VideoPlayer.pheinmage </a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字幕  </span> </p> </td> 
   <td colname="col2"> <p> 新字幕檔案的位置。 </p> <p>如果未指定，則註解按鈕在用戶介面中不可見。 以此參數指定的字幕會套用至媒體集中最先出現的影片。 後續視頻播放沒有字幕。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 傳回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

無。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

單媒體集參考：

```
<instance>.setAsset("Scene7SharedAssets/Mixed_Media_Set_Sample")
```

顯式媒體集：

```
<instance>.setAsset("Scene7SharedAssets/Backpack_J;;advanced_image;,Scene7SharedAssets/Frame-6;;advanced_image;,Scene7SharedAssets/Frame-2;;advanced_image;,Scene7SharedAssets/SpinSet_Sample;;spin;,Scene7SharedAssets/ImageSet-Colors-Sample;;advanced_swatchset;,Scene7SharedAssets/Glacier_Climber_640x360;Scene7SharedAssets/Glacier_Climber_640x360;video;")
```

集合中的所有影像都新增銳利化修飾元：

```
<instance>.setAsset("Scene7SharedAssets/Mixed_Media_Set_Sample?op_sharpen=1")
```
