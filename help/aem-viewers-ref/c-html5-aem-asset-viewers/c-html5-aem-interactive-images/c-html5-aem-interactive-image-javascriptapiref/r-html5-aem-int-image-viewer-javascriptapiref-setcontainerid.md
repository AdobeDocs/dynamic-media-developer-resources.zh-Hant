---
description: 視訊影像檢視器的JavaScript API參考。
seo-description: 視訊影像檢視器的JavaScript API參考。
seo-title: setContainerId
solution: Experience Manager
title: setContainerId
topic: Dynamic Media
uuid: f1486f82-28dd-4321-a0e5-9e5696f6bbf7
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 3%

---


# setContainerId{#setcontainerid}

視訊影像檢視器的JavaScript API參考。

` setContainerId( *`containerId`*)`

設定檢視器所插入之DOM容器（通常為DIV）的ID。 您不需要在呼叫此方法時建立容器元素。 但是，當`init()`執行時，容器必須存在。 必須在`init()`之前呼叫它。

如果檢視器設定資訊與`config` JSON物件一起傳遞至建構函式，此方法是選用的。

## 參數 {#section-fa807db629ce43bab286b1e1dc96c492}

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

