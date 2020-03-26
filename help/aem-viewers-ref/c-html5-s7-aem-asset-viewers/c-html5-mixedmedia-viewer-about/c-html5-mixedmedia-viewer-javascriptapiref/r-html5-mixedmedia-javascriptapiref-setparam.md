---
description: 混合媒體檢視器的JavaScript API參考。
seo-description: 混合媒體檢視器的JavaScript API參考。
seo-title: setParam
solution: Experience Manager
title: setParam
topic: Dynamic media
uuid: 427daeae-f7b4-4eb0-a285-e5b16c538239
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setParam{#setparam}

混合媒體檢視器的JavaScript API參考。

` setParam( *`名稱，值`*)`

將檢視器參數設定為指定值。 此參數為檢視器專用的設定選項或軟體開發套件修飾元。 此參數在之前被調用 `init()`。 如果檢視器設定資訊與 `config` JSON物件一起傳遞至建構函式，此方法為選用。

另請參見 [init](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-javascriptapiref/r-html5-mixedmedia-javascriptapiref-init.md#reference-bb4428c155e541b79797f96e17c068ae)。

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 名 <span class="varname"> 稱 </span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}參 </span> 數的名稱。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 值 <span class="varname"></span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}參 </span> 數的值。 值不能以百分比編碼。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

無。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParam("style", "customStyle.css")
```

