---
description: 視訊檢視器的JavaScript API參考。
seo-description: 視訊檢視器的JavaScript API參考。
seo-title: setAsset
solution: Experience Manager
title: setAsset
topic: Dynamic media
uuid: f106b3d4-880e-4ba3-ae47-a005af5c0f1b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setAsset{#setasset}

視訊檢視器的JavaScript API參考。

` setAsset( *`asset`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 資產 </span></span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> String </span>}新資產ID、明確影像集或具有影格特定影像伺服修飾元的明確影像集，以及附加在"?"之後的選用全域影像伺服修飾元。 </p> <p> 此檢視器不支援使用IR（影像演算）或UGC（使用者產生的內容）的影像。 </p> </td> 
  </tr> 
 </tbody> 
</table>

設定新資產。 您可以隨時呼叫此參數，不論是在之前或之後 `init()`。 如果在之後呼叫，檢 `init()`視器會在執行時期交換資產。

另請參見 [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-javascriptapiref/r-html5-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)。

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

無。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

單一影像參考：

```
 <instance>.setAsset("Scene7SharedAssets/Backpack_B")
```

對目錄中定義的影像集的單一參考：

```
 <instance>.setAsset("Scene7SharedAssets/ImageSet-Views-Sample")
```

顯式影像集：

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C")
```

使用影格特定影像伺服修飾元的顯式影像集：

```
 <instance>.setAsset("(Scene7SharedAssets/Backpack_B?op_colorize=255%2C0%2C0,Scene7SharedAssets/Backpack_B?op_colorize=0x00ff00)")
```

銳利化修飾元已新增至該集中的所有影像：

```
 <instance>.setAsset("Scene7SharedAssets/ImageSet-Views-Sample?op_sharpen=1")
```

