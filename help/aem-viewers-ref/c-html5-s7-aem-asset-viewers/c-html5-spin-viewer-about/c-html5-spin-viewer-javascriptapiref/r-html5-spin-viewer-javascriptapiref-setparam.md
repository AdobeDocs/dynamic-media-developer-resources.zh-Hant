---
description: 回轉檢視器的JavaScript API參考。
seo-description: 回轉檢視器的JavaScript API參考。
seo-title: setParam
solution: Experience Manager
title: setParam
topic: Dynamic Media
uuid: 5f7be1d4-28aa-497c-9067-853c227aa11a
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 2%

---


# setParam{#setparam}

回轉檢視器的JavaScript API參考。

` setParam( *`名稱，值`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 名稱  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}參 </span> 數的名稱。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 值  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}參 </span> 數值。值不能以百分比編碼。 </p> </td> 
  </tr> 
 </tbody> 
</table>

將檢視器參數設定為指定值。 此參數為檢視器專用的設定選項或軟體開發套件修飾元。 此參數在`init()`之前被呼叫。

如果檢視器設定資訊與`config` JSON物件一起傳遞至建構函式，此方法為選用。

另請參閱[init](../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-javascriptapiref/r-html5-spin-viewer-javascriptapiref-init.md#reference-bb4428c155e541b79797f96e17c068ae)。

## 傳回{#section-1d3cf85bc7cc4dfe9670e038d02b9101}

無。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParam("style", "customStyle.css")
```

