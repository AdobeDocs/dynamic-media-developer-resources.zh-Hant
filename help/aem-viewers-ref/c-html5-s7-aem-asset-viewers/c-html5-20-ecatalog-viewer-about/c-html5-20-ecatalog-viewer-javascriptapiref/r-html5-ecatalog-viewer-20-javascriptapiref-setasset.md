---
title: 設定資產
description: 視頻查看器的JavaScript API參考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 04b6bf4d-5c42-49e9-b585-de75ebf6c89f
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 2%

---

# 設定資產{#setasset}

視頻查看器的JavaScript API參考。

` setAsset( *`asset`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 資產 </span> </span> </p> </td> 
   <td colname="col2"> <p>{ 0} <span class="codeph"> 字串 </span>}新資產ID或顯式影像集，並附加可選的Image Service修飾符 <span class="codeph"> ? </span>。 </p> <p> 此查看器不支援使用IR（影像呈現）或UGC（用戶生成的內容）的影像。 </p> </td> 
  </tr> 
 </tbody> 
</table>

設定新資產。 可以在任何時間（在之前或之後）調用此參數 `init()`。 如果在 `init()`，查看器在運行時交換資產。

另請參閱 [初始化](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)。

## 返回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

無。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

對目錄中定義的影像集的單個引用：

```
 <instance>.setAsset("Viewers/Pluralist")
```

具有預組合頁的顯式影像集：

```
 <instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C,Scene7SharedAssets/Backpack_H,Scene7SharedAssets/Backpack_J")
```

顯式影像集，包含各個頁面影像：

```
 <instance>.setAsset("Scene7SharedAssets/AdobeScene7_Overview_US-1,Scene7SharedAssets/AdobeScene7_Overview_US-2:AdobeScene7_Overview_US-3,Scene7SharedAssets/AdobeScene7_Overview_US-4")
```

銳化修飾符添加到集中的所有影像：

```
 <instance>.setAsset("Viewers/Pluralist?op_sharpen=1")
```
