---
description: Video360檢視器的JavaScript API參考。
seo-description: Video360檢視器的JavaScript API參考。
seo-title: setAsset
solution: Experience Manager
title: setAsset
topic: Dynamic media
uuid: db1321fb-6d52-4add-8877-0c13eb12e6af
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setAsset{#setasset}

Video360檢視器的JavaScript API參考。

`setAsset(asset)`

設定新資產。 您可以隨時呼叫此參數，不論是在之前或之後 `init()`。 如果在之後呼叫，檢 `init()`視器會在執行時期交換資產。

另請參見 [init](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-javascriptapiref/r-html5-aem-video360-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)。

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> asset </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph"> String</span>}新資產ID。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

無。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setAsset("Viewers/space_station_360-AVS")
```

