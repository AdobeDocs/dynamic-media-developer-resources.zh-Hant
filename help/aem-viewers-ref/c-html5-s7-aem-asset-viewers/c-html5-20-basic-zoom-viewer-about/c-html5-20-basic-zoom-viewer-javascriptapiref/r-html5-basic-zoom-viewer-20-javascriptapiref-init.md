---
description: 基本縮放檢視器的JavaScript API參考。
solution: Experience Manager
title: init
feature: Dynamic Media Classic，檢視器，SDK/API，縮放
role: Developer,Business Practitioner
exl-id: cef585ae-44d7-406c-96f9-e03959a8e518
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 2%

---

# init{#init}

基本縮放檢視器的JavaScript API參考。

`init()`

啟動基本縮放查看器的初始化。 此時必須建立容器DOM元素，檢視器程式碼才能透過其ID找到它。

如果容器元素尚未屬於網頁版面的一部分（例如，可能會使用指派給它的`display:none`樣式來隱藏），則檢視器會暫停其初始化程式，直到網頁將容器元素帶回版面的那一刻為止。 發生此情況時，檢視器載入會自動恢復。

在檢視器生命週期期間，只需呼叫此方法一次；會忽略後續呼叫。

## 參數 {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

無。

## 傳回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` 檢視器例項的參考。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
