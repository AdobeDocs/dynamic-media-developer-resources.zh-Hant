---
description: 視訊檢視器的JavaScript API參考。
seo-description: 視訊檢視器的JavaScript API參考。
seo-title: setContainerId
solution: Experience Manager
title: setContainerId
uuid: ac3419c0-180d-4e5c-935f-643495a01268
feature: Dynamic Media經典，檢視器，SDK/API，縮放
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 1%

---


# setContainerId{#setcontainerid}

視訊檢視器的JavaScript API參考。

` setContainerId( *`containerId`*)`

設定檢視器所插入之DOM容器（通常為DIV）的ID。 您不需要在呼叫此方法時建立容器元素。 但是，當`init()`執行時，容器必須存在。 必須在`init()`之前呼叫它。

如果檢視器設定資訊與`config` JSON物件一起傳遞給建構函式，此方法是選用的。

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> containerId  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}容 </span> 器的ID。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 傳回{#section-1d3cf85bc7cc4dfe9670e038d02b9101}

無。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setContainerId("s7viewer");
```

