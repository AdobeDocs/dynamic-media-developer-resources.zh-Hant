---
description: 互動式視訊檢視器的JavaScript API參考。
seo-description: 互動式視訊檢視器的JavaScript API參考。
seo-title: setParam
solution: Experience Manager
title: setParam
uuid: c8c40e88-530f-4af8-be9a-2e88addd6907
feature: Dynamic Media經典，檢視器，SDK/API，互動式視訊
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 2%

---


# setParam{#setparam}

互動式視訊檢視器的JavaScript API參考。

` setParam( *`名稱，值`*)`

將檢視器參數設定為指定值。 此參數為檢視器專用的設定選項或軟體開發套件修飾元。 此參數在`init()`之前被呼叫。

如果檢視器設定資訊與`config` JSON物件一起傳遞給建構函式，此方法是選用的。

另請參閱[init](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)。

## 參數 {#section-c68a5a3688d342fd9d6a7fd59867cc7a}

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

## 傳回{#section-1d3cf85bc7cc4dfe9670e038d02b9101}

無。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParam("style", "customStyle.css")
```

