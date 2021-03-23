---
description: 視訊檢視器的JavaScript API參考。
seo-description: 視訊檢視器的JavaScript API參考。
seo-title: setAsset
solution: Experience Manager
title: setAsset
uuid: f106b3d4-880e-4ba3-ae47-a005af5c0f1b
feature: Dynamic Media經典，檢視器，SDK/API，縮放
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 2%

---


# setAsset{#setasset}

視訊檢視器的JavaScript API參考。

` setAsset( *`asset`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 資產  </span> </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph">字串</span>}新資產ID、明確影像集或明確影像集（含影格特定的影像伺服修飾元），以及附加在"?"之後的選用全域影像伺服修飾元。 </p> <p> 此檢視器不支援使用IR（影像演算）或UGC（使用者產生的內容）的影像。 </p> </td> 
  </tr> 
 </tbody> 
</table>

設定新資產。 您可以隨時在`init()`之前或之後呼叫此參數。 如果在`init()`之後呼叫，檢視器會在執行時期交換資產。

另請參閱[init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-javascriptapiref/r-html5-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)。

## 傳回{#section-1d3cf85bc7cc4dfe9670e038d02b9101}

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

