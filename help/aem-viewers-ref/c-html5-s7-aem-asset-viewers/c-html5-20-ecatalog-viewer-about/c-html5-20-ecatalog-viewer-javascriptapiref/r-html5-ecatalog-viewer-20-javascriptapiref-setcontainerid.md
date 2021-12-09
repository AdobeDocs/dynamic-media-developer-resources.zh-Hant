---
title: setContainerId
description: eCatalog檢視器的JavaScript API參考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 32e75d36-cc9a-42df-95e8-5b48456296e9
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 2%

---

# setContainerId{#setcontainerid}

eCatalog檢視器的JavaScript API參考。

` setContainerId( *`containerId`*)`

設定 `DOM` 容器(通常為 `DIV`)，檢視器會插入其中。 呼叫此方法時，不需要建立容器元素。 然而，容器必須存在於 `init()` 執行中。 必須在之前呼叫 `init()`.

如果檢視器設定資訊是以 `config` JSON物件至建構函式。

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> containerId </span> </span> </p> </td> 
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
