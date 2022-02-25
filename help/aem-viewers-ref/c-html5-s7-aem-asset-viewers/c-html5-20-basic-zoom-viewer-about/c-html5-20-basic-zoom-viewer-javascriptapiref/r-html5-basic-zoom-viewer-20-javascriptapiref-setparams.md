---
title: setParams
description: 用於基本縮放查看器的JavaScript API參考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: f142dd72-5e45-44f6-a79b-3eaf6a310bde
source-git-commit: 7eddc50fb9803eacdd1f513c6132380793b6f88d
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 2%

---

# setParams{#setparams}

用於基本縮放查看器的JavaScript API參考。

` setParams( *`帕拉`*)`

將一個或多個參數設定為給定值。 方法參數語法與URL查詢字串相同。 即，它表示與 `&`。 與查詢字串一樣，名稱和值使用UTF8進行百分比編碼。 在你打電話之前 `init()`，必須調用此參數。

如果與一起傳遞了查看器配置資訊，則此方法是可選的 `config` JSON對象到建構子。

另請參閱 [初始化](../../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-javascriptapiref/r-html5-basic-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)。

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 帕拉</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}</span> name=value參數對，分隔為 <span class="codeph"> &amp;</span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 返回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

無。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParams("ZoomView.zoomfactor=2,3&ZoomView.iscommand=op_sharpen%3d1")
```
