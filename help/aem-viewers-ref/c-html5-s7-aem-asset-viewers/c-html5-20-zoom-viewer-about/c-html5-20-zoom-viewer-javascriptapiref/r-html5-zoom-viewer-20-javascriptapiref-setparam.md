---
description: 視訊檢視器的JavaScript API參考。
solution: Experience Manager
title: setParam
feature: Dynamic Media Classic，檢視器，SDK/API，縮放
role: Developer,Business Practitioner
exl-id: d797a8be-582e-46f4-9068-db1d2757970d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 2%

---

# setParam{#setparam}

視訊檢視器的JavaScript API參考。

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

如果檢視器設定資訊是以`config` JSON物件傳遞至建構函式，則此方法為選用。

另請參閱[init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-javascriptapiref/r-html5-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)。

## 傳回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

無。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParam("style", "customStyle.css")
```
