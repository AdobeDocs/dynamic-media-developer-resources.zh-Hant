---
description: 混合媒體檢視器的JavaScript API參考。
solution: Experience Manager
title: setParams
feature: Dynamic Media Classic，檢視器，SDK/API，混合媒體集
role: Developer,Business Practitioner
exl-id: 200805ca-20e5-4d3a-90ba-2511e71705ab
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 1%

---

# setParams{#setparams}

混合媒體檢視器的JavaScript API參考。

` setParams( *`params`*)`

將一或多個參數設為指定值。 方法引數語法與URL查詢字串相同。 也就是說，它表示以`&`分隔的名稱=值配對。 就像在查詢字串中一樣，名稱和值是使用UTF8進行百分比編碼。 呼叫`init()`之前，必須呼叫此參數。 如果將檢視器配置資訊與`config` JSON物件傳遞至建構函式，則此方法為選用。

另請參閱[init](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-javascriptapiref/r-html5-mixedmedia-javascriptapiref-init.md#reference-bb4428c155e541b79797f96e17c068ae)。

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> params</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}</span> name=value參數對(以&amp; <span class="codeph"> 分隔)</span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 傳回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

無。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParams("ZoomView.zoomstep=2,3&ZoomView.iscommand=op_sharpen%3d1")
```
