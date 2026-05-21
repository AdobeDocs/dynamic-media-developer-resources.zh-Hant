---
title: setParam
description: 全景檢視器的JavaScript API參考。
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
autotag-review: '2026-05-13T22:11:37.806Z'
TQID: 'https://experienceleague.adobe.com/Hw4SgeJ8yTvGg1zDyDkqtWH6gfGdIHa0daPZ7cT6eow'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
source-git-commit: e76d4c499daf8c8a7a0be31e56d84f917c643095
workflow-type: tm+mt
source-wordcount: 80
ht-degree: 2%

---

# setParam{#setparam}

全景檢視器的JavaScript API參考。

` setParam( *`名稱，值`*)`

將檢視器引數設定為指定的值。 引數是檢視器特定的組態選項或軟體開發套件修飾元。 在`init()`之前呼叫此引數。

如果檢視器組態資訊是與`config` JSON物件一併傳遞給建構函式，則此方法為選用。



<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">名稱</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}引數的</span>名稱。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">值</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}引數的</span>值。 值不得以百分比編碼。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 傳回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

無。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParam("style", "customStyle.css")
```
