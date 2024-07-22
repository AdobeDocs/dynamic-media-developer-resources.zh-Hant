---
title: setParam
description: 影片檢視器的JavaScript API參考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: d797a8be-582e-46f4-9068-db1d2757970d
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 2%

---

# setParam{#setparam}

影片檢視器的JavaScript API參考。

` setParam( *`名稱，值`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">名稱</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} </span>引數名稱。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">值</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} </span>引數值。 值不得以百分比編碼。 </p> </td> 
  </tr> 
 </tbody> 
</table>

將檢視器引數設定為指定的值。 引數是檢視器特定的組態選項或軟體開發套件修飾元。 在`init()`之前呼叫此引數。

如果檢視器組態資訊已與`config` JSON物件一併傳遞給建構函式，則此方法為選用。

另請參閱[init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-javascriptapiref/r-html5-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)。

## 傳回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

無。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParam("style", "customStyle.css")
```
