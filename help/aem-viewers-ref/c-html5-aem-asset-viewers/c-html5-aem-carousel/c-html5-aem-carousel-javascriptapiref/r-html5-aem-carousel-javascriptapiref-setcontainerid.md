---
description: 輪播檢視器的JavaScript API參考。
solution: Experience Manager
title: setContainerId
feature: Dynamic Media Classic，檢視器，SDK/API，輪播橫幅
role: Developer,User
exl-id: 32636cf9-3dc7-4299-a7b7-cf803ca36514
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 3%

---

# setContainerId{#setcontainerid}

輪播檢視器的JavaScript API參考。

` setContainerId( *`containerId`*)`

設定檢視器所插入的DOM容器ID（通常為`DIV`）。 呼叫此方法時，不需要建立容器元素。 但是，當`init()`運行時，容器必須存在。 必須在`init()`之前呼叫。

如果將檢視器配置資訊與`config` JSON對象一併傳遞給建構子，則此方法為可選。

## 參數 {#section-fa807db629ce43bab286b1e1dc96c492}

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
