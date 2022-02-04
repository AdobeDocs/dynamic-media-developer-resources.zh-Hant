---
title: setContainerId
description: 用於Spin Viewer的JavaScript API參考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 5859800f-7d01-4c32-a67f-211578d5c50b
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 2%

---

# setContainerId{#setcontainerid}

用於Spin Viewer的JavaScript API參考。

` setContainerId( *`容器ID`*)`

設定DOM容器（通常為DIV）的ID，查看器將插入其中。 不必在調用此方法時建立容器元素。 但是，當 `init()` 。 必須在之前調用 `init()`。

如果與一起傳遞查看器配置資訊，則此方法是可選的 `config` 建構子的JSON對象。

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
