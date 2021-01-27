---
description: 視訊影像檢視器的JavaScript API參考。
seo-description: 視訊影像檢視器的JavaScript API參考。
seo-title: setAsset
solution: Experience Manager
title: setAsset
topic: Dynamic Media
uuid: 8cb10b2e-addb-4659-a93b-5a53d0f8a5bb
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 3%

---


# setAsset{#setasset}

視訊影像檢視器的JavaScript API參考。

` setAsset( *`asset`*)`

設定新資產。 您可以隨時在`init()`之前或之後呼叫此參數。 如果在`init()`之後呼叫，檢視器會在執行時期交換資產。

另請參閱[init](../../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-javascriptapiref/r-html5-aem-int-image-viewer-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)。

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 資產</span> </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph">字串</span>}新資產ID。 </p> <p>此檢視器不支援使用IR（影像演算）或UGC（使用者產生的內容）的影像。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 傳回{#section-1d3cf85bc7cc4dfe9670e038d02b9101}

無。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

單一影像參考：

```
<instance>.setAsset("/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg")
```

