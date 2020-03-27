---
description: 回轉檢視器的JavaScript API參考。
seo-description: 回轉檢視器的JavaScript API參考。
seo-title: setParams
solution: Experience Manager
title: setParams
topic: Dynamic media
uuid: f0eedfbd-eb32-49db-bca4-cc7b14d5495e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setParams{#setparams}

回轉檢視器的JavaScript API參考。

` setParams( *`params`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> params</span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}</span> name=value參數對，與&amp; <span class="codeph"> 分隔</span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

將一個或多個參數設定為給定值。 方法引數語法與URL查詢字串相同。 也就是說，它表示與分隔的name=value對 `&`。 與查詢字串一樣，名稱和值使用UTF8進行百分比編碼。 在呼叫之 `init()`前，必須呼叫此參數。

如果檢視器設定資訊與 `config` JSON物件一起傳遞至建構函式，此方法為選用。

另請參見 [init](../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-javascriptapiref/r-html5-spin-viewer-javascriptapiref-init.md#reference-bb4428c155e541b79797f96e17c068ae)。

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

無。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParams("SpinView.zoomstep=2,3&SpinView.iscommand=op_sharpen%3d1")
```

