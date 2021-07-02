---
description: 混合媒體檢視器的JavaScript API參考。
solution: Experience Manager
title: init
feature: Dynamic Media Classic，檢視器，SDK/API，混合媒體集
role: Developer,Business Practitioner
exl-id: 4fb40cec-172a-41b3-98fc-927da88c7cb9
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 2%

---

# init{#init}

混合媒體檢視器的JavaScript API參考。

`init()`

啟動混合媒體查看器的初始化。 此時必須建立容器DOM元素，檢視器程式碼才能透過其ID找到它。

如果容器元素尚未屬於網頁版面的一部分（例如，可能會使用指派給它的`display:none`樣式來隱藏），則檢視器會暫停其初始化程式，直到網頁將容器元素帶回版面的那一刻為止。 發生此情況時，檢視器載入會自動恢復。

在檢視器生命週期期間，只呼叫此方法一次；會忽略後續呼叫。

## 參數 {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

無。

## 傳回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` 檢視器例項的參考。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
