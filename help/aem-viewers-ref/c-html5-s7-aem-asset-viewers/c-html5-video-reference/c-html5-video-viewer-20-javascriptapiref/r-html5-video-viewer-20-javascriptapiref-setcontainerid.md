---
title: setContainerId
description: 視頻查看器的JavaScript API參考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 9f2857a4-108d-4689-9c39-cb2635405d0d
source-git-commit: 11acb9151d3ea247eecde3cfbbd295a95c10829c
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 2%

---

# setContainerId{#setcontainerid}

視頻查看器的JavaScript API參考。

` setContainerId( *`容器ID`*)`

設定DOM容器的ID(通常為 `DIV`)。 不必在調用此方法時建立容器元素。 但是，當 `init()` 。 此參數在 `init()`。 如果與一起傳遞查看器配置資訊，則此方法是可選的 `config` 建構子的JSON對象。

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 容器ID </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} </span> 容器ID。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 返回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

無。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setContainerId("s7viewer");
```
