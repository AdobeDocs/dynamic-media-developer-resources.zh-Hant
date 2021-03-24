---
description: eCatalog檢視器的JavaScript API參考。
solution: Experience Manager
title: setParams
feature: Dynamic Media經典，檢視器，SDK/API,eCatalog搜尋
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '108'
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

