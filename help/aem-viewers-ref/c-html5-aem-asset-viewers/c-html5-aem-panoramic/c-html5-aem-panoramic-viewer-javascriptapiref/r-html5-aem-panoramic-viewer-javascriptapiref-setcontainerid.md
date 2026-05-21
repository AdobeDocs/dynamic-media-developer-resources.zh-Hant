---
title: setContainerId
description: 全景檢視器的JavaScript API參考。
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: b0145fb0-2b0d-40ce-ac18-029f54bc4050
autotag-review: '2026-05-13T22:10:33.187Z'
TQID: 'https://experienceleague.adobe.com/4Ndg-s-4Re6hMADDbkBDvKWdGFH8bzHGGooU-rNCraU'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
source-git-commit: e76d4c499daf8c8a7a0be31e56d84f917c643095
workflow-type: tm+mt
source-wordcount: 88
ht-degree: 3%

---

# setContainerId{#setcontainerid}

全景檢視器的JavaScript API參考。

` setContainerId( *`containerId`*)`

設定檢視器插入其中的DOM容器（通常是DIV）的ID。 不需要在呼叫此方法時建立容器元素。 但是，執行`init()`時容器必須存在。 必須在`init()`之前呼叫它。

如果檢視器組態資訊與`config` JSON物件一起傳遞至建構函式，則此方法為選用。

## 參數 {#section-fa807db629ce43bab286b1e1dc96c492}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> containerId </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}容器的</span> ID。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 傳回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

無。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setContainerId("s7viewer");
```
