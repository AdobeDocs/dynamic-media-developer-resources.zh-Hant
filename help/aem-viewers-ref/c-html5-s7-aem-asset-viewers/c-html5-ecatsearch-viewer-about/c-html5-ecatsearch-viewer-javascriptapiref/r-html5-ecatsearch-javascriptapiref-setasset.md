---
description: 視訊檢視器的JavaScript API參考。
seo-description: 視訊檢視器的JavaScript API參考。
seo-title: setAsset
solution: Experience Manager
title: setAsset
topic: Dynamic media
uuid: ab078f32-c523-4b6c-a0d6-45dd2af35b36
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4

---


# setAsset{#setasset}

視訊檢視器的JavaScript API參考。

[!DNL ` setAsset( *`asset`*)`]

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 資產 </span></span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> String </span>}新資產ID或明確影像集，並附加選用的影像伺服修飾元 <span class="codeph"> ? </span>。 </p> <p> 此檢視器不支援使用IR（影像演算）或UGC（使用者產生的內容）的影像。 </p> </td> 
  </tr> 
 </tbody> 
</table>

設定新資產。 您可以隨時呼叫此參數，不論是在之前或之後 [!DNL `init()`]。 如果在之後呼叫，檢 [!DNL `init()`]視器會在執行時期交換資產。

另請參見 [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)。

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

無。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

對目錄中定義的影像集的單一參考：

```
 <instance>.setAsset("Viewers/Pluralist")
```

明確的影像集，預先組合頁面：

```
 <instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C,Scene7SharedAssets/Backpack_H,Scene7SharedAssets/Backpack_J")
```

明確的影像集，包含個別的頁面影像：

```
 <instance>.setAsset("Scene7SharedAssets/AdobeScene7_Overview_US-1,Scene7SharedAssets/AdobeScene7_Overview_US-2:AdobeScene7_Overview_US-3,Scene7SharedAssets/AdobeScene7_Overview_US-4")
```

銳利化修飾元已新增至該集中的所有影像：

```
 <instance>.setAsset("Viewers/Pluralist?op_sharpen=1")
```

