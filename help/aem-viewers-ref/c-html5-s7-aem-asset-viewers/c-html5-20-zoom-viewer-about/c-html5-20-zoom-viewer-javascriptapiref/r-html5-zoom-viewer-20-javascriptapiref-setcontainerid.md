---
description: 視訊檢視器的JavaScript API參考。
seo-description: 視訊檢視器的JavaScript API參考。
seo-title: setContainerId
solution: Experience Manager
title: setContainerId
topic: Dynamic media
uuid: ac3419c0-180d-4e5c-935f-643495a01268
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setContainerId{#setcontainerid}

視訊檢視器的JavaScript API參考。

` setContainerId( *`containerId`*)`

設定檢視器所插入之DOM容器（通常為DIV）的ID。 您不需要在呼叫此方法時建立容器元素。 但是，容器在執行時必 `init()` 須存在。 必須先呼叫 `init()`。

如果檢視器設定資訊是與 `config` JSON物件一起傳遞至建構函式，此方法為選用。

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 容 <span class="varname"> 器ID </span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}容 </span> 器的ID。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

無。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setContainerId("s7viewer");
```

