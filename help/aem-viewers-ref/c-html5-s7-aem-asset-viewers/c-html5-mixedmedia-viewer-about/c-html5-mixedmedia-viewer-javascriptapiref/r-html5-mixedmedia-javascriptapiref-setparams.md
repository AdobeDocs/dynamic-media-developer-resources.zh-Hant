---
description: 混合媒體檢視器的JavaScript API參考。
seo-description: 混合媒體檢視器的JavaScript API參考。
seo-title: setParams
solution: Experience Manager
title: setParams
topic: Dynamic media
uuid: 46db0ce3-fd70-4577-92ed-e7d2d15e0dab
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 1%

---


# setParams{#setparams}

混合媒體檢視器的JavaScript API參考。

` setParams( *`params`*)`

將一個或多個參數設定為給定值。 方法引數語法與URL查詢字串相同。 即，它表示與`&`分隔的name=value對。 與查詢字串一樣，名稱和值使用UTF8進行百分比編碼。 在呼叫`init()`之前，必須呼叫此參數。 如果檢視器設定資訊與`config` JSON物件一起傳遞至建構函式，此方法為選用。

另請參閱[init](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-javascriptapiref/r-html5-mixedmedia-javascriptapiref-init.md#reference-bb4428c155e541b79797f96e17c068ae)。

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> params</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}</span> name=value參數對與&amp;分 <span class="codeph"> 隔</span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 傳回{#section-1d3cf85bc7cc4dfe9670e038d02b9101}

無。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParams("ZoomView.zoomstep=2,3&ZoomView.iscommand=op_sharpen%3d1")
```

