---
description: 輪播檢視器的JavaScript API參考。
solution: Experience Manager
title: setAsset
feature: Dynamic Media Classic，檢視器，SDK/API，輪播橫幅
role: Developer,User
exl-id: e8aaee4e-56d5-46e4-8499-d5c9a6ba5d3b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 3%

---

# setAsset{#setasset}

輪播檢視器的JavaScript API參考。

` setAsset( *`asset`*)`

設定新資產。 您可以在`init()`之前或之後隨時呼叫此參數。 如果在`init()`之後呼叫，檢視器會在執行階段交換資產。

另請參閱[init](../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-javascriptapiref/r-html5-aem-carousel-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)。

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 資產</span> </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph">字串</span>}新資產ID。 </p> <p>此檢視器不支援使用IR（影像轉譯）或UGC（使用者產生的內容）的影像。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 傳回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

無。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

單一影像參考：

```
<instance>.setAsset("/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner")
```
