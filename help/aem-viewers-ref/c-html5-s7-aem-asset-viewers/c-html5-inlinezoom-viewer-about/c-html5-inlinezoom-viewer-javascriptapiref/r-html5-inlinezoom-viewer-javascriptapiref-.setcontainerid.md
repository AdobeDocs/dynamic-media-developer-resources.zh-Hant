---
title: setContainerId
description: 內嵌縮放檢視器的JavaScript API參考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: ab3359f0-0c58-4984-815a-e0246728100e
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 2%

---

# setContainerId{#setcontainerid}

內嵌縮放檢視器的JavaScript API參考。

` setContainerId( *`containerId`*)`

設定DOM容器的ID(通常為 `DIV`)，檢視器會插入其中。 呼叫此方法時，不需要建立容器元素。 然而，容器必須存在於 `init()` 執行中。 必須在之前呼叫 `init()`. 如果檢視器設定資訊是以 `config` JSON物件至建構函式。

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
