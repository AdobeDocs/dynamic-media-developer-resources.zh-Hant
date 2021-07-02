---
description: 混合媒體檢視器的JavaScript API參考。
solution: Experience Manager
title: setContainerId
feature: Dynamic Media Classic，檢視器，SDK/API，混合媒體集
role: Developer,Business Practitioner
exl-id: b6e191dc-3172-45ba-b6f6-258cfbd5855d
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 2%

---

# setContainerId{#setcontainerid}

混合媒體檢視器的JavaScript API參考。

` setContainerId( *`containerId`*)`

設定檢視器所插入的DOM容器ID（通常為DIV）。 呼叫此方法時，不需要建立容器元素。 但是，當`init()`運行時，容器必須存在。 必須在`init()`之前呼叫。 如果將檢視器配置資訊與`config` JSON物件傳遞至建構函式，則此方法為選用。

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> containerId  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} </span> 容器ID。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 傳回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

無。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setContainerId("s7viewer");
```
