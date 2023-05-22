---
title: 設定資產
description: 用於混合媒體查看器的JavaScript API參考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 3ad78de9-17a6-40c9-b389-a1f7eed11635
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 1%

---

# 設定資產{#setasset}

用於混合媒體查看器的JavaScript API參考。

` setAsset( *`asset`*[,data]))`

設定新資產和可選附加資產資料。 可以在任何時間（在之前或之後）調用此參數 `init()`。 如果在 `init()`，查看器在運行時交換資產。

另請參閱 [初始化](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-javascriptapiref/r-html5-mixedmedia-javascriptapiref-init.md#reference-bb4428c155e541b79797f96e17c068ae)。

## 參數 {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

`*`資產`*` - { `String`}新資產ID或顯式混合媒體集，在後面附加可選的「影像服務」修改符 `?`。

此查看器不支援使用IR（影像呈現）或UGC（用戶生成的內容）的影像。

`*`資料`*` - { `JSON`}新標題檔案的位置。

如果未指定，則說明按鈕在用戶介面中不可見。 使用此參數指定的字幕適用於混合媒體集中最先出現的視頻；隨後播放的視頻沒有字幕。 此查看器支援以下元件ID:

<table id="table_7B5DD9303EF44ADD847B13FFEAD135D9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>元件ID </p> </th> 
   <th colname="col2" class="entry"> <p>查看器SDK元件類名 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 後驗 </span> </p> </td> 
   <td colname="col2"> <p>在視頻開始播放之前，要在第一幀上顯示的影像。 </p> <p>請參閱 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/r-html5-mixedmedia-viewer-config-attrib/r-html5-mixedmedia-viewer-config-attrib-videoplayer-posterimage.md#reference-f424ad0f278b4d14b86ea55e3a73c52b" format="dita" scope="local"> VideoPlayer.後驗影像 </a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字幕 </span> </p> </td> 
   <td colname="col2"> <p> 新標題檔案的位置。 </p> <p>如果未指定，則說明按鈕在用戶介面中不可見。 使用此參數指定的字幕應用於媒體集中最先出現的視頻。 後續視頻播放時沒有字幕。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 返回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

無。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

單媒體集引用：

```
<instance>.setAsset("Scene7SharedAssets/Mixed_Media_Set_Sample")
```

顯式媒體集：

```
<instance>.setAsset("Scene7SharedAssets/Backpack_J;;advanced_image;,Scene7SharedAssets/Frame-6;;advanced_image;,Scene7SharedAssets/Frame-2;;advanced_image;,Scene7SharedAssets/SpinSet_Sample;;spin;,Scene7SharedAssets/ImageSet-Colors-Sample;;advanced_swatchset;,Scene7SharedAssets/Glacier_Climber_640x360;Scene7SharedAssets/Glacier_Climber_640x360;video;")
```

銳化修飾符添加到集中的所有影像：

```
<instance>.setAsset("Scene7SharedAssets/Mixed_Media_Set_Sample?op_sharpen=1")
```
