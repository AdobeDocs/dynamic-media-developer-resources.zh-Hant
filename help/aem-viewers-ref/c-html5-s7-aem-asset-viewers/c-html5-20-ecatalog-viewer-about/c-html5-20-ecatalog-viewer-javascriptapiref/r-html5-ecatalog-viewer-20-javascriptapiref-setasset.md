---
description: 視訊檢視器的JavaScript API參考。
solution: Experience Manager
title: setAsset
feature: Dynamic Media Classic，檢視器，SDK/API,eCatalog
role: Developer,Business Practitioner
exl-id: 04b6bf4d-5c42-49e9-b585-de75ebf6c89f
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 2%

---

# setAsset{#setasset}

視訊檢視器的JavaScript API參考。

` setAsset( *`asset`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 資產  </span> </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph">字串</span>}新資產ID或顯式影像集，附加在<span class="codeph">後的可選影像伺服修飾元？</span>。 </p> <p> 此檢視器不支援使用IR（影像轉譯）或UGC（使用者產生的內容）的影像。 </p> </td> 
  </tr> 
 </tbody> 
</table>

設定新資產。 您可以在`init()`之前或之後隨時呼叫此參數。 如果在`init()`之後呼叫，檢視器會在執行階段交換資產。

另請參閱[init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)。

## 傳回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

無。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

對目錄中定義的影像集的單個引用：

```
 <instance>.setAsset("Viewers/Pluralist")
```

明確影像集，並預先組合頁面：

```
 <instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C,Scene7SharedAssets/Backpack_H,Scene7SharedAssets/Backpack_J")
```

明確影像集，包含個別頁面影像：

```
 <instance>.setAsset("Scene7SharedAssets/AdobeScene7_Overview_US-1,Scene7SharedAssets/AdobeScene7_Overview_US-2:AdobeScene7_Overview_US-3,Scene7SharedAssets/AdobeScene7_Overview_US-4")
```

集合中的所有影像都新增銳利化修飾元：

```
 <instance>.setAsset("Viewers/Pluralist?op_sharpen=1")
```
