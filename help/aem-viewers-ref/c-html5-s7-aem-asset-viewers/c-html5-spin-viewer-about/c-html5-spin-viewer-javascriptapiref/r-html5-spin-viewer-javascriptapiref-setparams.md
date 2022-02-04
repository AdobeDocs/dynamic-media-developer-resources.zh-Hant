---
title: setParams
description: 用於Spin Viewer的JavaScript API參考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 61d5b791-12bd-444a-add1-5537c71881fe
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 2%

---

# setParams{#setparams}

用於Spin Viewer的JavaScript API參考。

` setParams( *`帕拉`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 帕拉</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}</span> name=value參數對，分隔為 <span class="codeph"> &amp;</span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

將一個或多個參數設定為給定值。 方法參數語法與URL查詢字串相同。 即，它表示與 `&`。 與查詢字串一樣，名稱和值使用UTF8進行百分比編碼。 在你打電話之前 `init()`，必須調用此參數。

如果與一起傳遞查看器配置資訊，則此方法是可選的 `config` 建構子的JSON對象。

另請參閱 [初始化](../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-javascriptapiref/r-html5-spin-viewer-javascriptapiref-init.md#reference-bb4428c155e541b79797f96e17c068ae)。

## 返回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

無。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParams("SpinView.zoomstep=2,3&SpinView.iscommand=op_sharpen%3d1")
```
