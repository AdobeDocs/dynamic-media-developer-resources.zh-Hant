---
description: 回轉檢視器的JavaScript API參考。
solution: Experience Manager
title: setParam
feature: Dynamic Media Classic，檢視器，SDK/API，回轉集
role: Developer,Business Practitioner
exl-id: 16d1d2cd-f58f-4ac3-b89f-f2f12fee231d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 2%

---

# setParam{#setparam}

回轉檢視器的JavaScript API參考。

` setParam( *`名稱，值`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 名稱  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} </span> 參數名稱。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> value  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 參數的 </span> {string}值。值無法以百分比編碼。 </p> </td> 
  </tr> 
 </tbody> 
</table>

將檢視器參數設為指定值。 參數為查看器特定配置選項或軟體開發套件修改器。 此參數在`init()`之前呼叫。

如果將檢視器配置資訊與`config` JSON物件傳遞至建構函式，則此方法為選用。

另請參閱[init](../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-javascriptapiref/r-html5-spin-viewer-javascriptapiref-init.md#reference-bb4428c155e541b79797f96e17c068ae)。

## 傳回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

無。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParam("style", "customStyle.css")
```
