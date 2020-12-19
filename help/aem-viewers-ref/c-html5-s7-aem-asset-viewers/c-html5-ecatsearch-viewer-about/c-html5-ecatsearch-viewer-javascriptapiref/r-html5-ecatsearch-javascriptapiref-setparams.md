---
description: eCatalog檢視器的JavaScript API參考。
seo-description: eCatalog檢視器的JavaScript API參考。
seo-title: setParams
solution: Experience Manager
title: setParams
topic: Dynamic media
uuid: 4929884e-b072-4177-83c3-1f9b4e5df569
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 1%

---


# setParams{#setparams}

eCatalog檢視器的JavaScript API參考。

[!DNL ` setParams( *`params`*)`]

將一個或多個參數設定為給定值。 方法引數語法與URL查詢字串相同。 即，它表示與[!DNL `&`]分隔的name=value對。 與查詢字串一樣，名稱和值使用UTF8進行百分比編碼。 在呼叫[!DNL `init()`]之前，必須呼叫此參數。

如果檢視器設定資訊與[!DNL `config`] JSON物件一起傳遞至建構函式，此方法為選用。

另請參閱[init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)。

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
<instance>.setParams("PageView.zoomstep=2,3&PageView.iscommand=op_sharpen%3d1")
```

