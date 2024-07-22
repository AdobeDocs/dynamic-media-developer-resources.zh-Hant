---
title: init
description: 混合媒體檢視器的JavaScript API參考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 4fb40cec-172a-41b3-98fc-927da88c7cb9
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 2%

---

# init{#init}

混合媒體檢視器的JavaScript API參考。

`init()`

開始初始化混合媒體檢視器。 此時，必須建立容器DOM元素，讓檢視器程式碼可依其ID尋找。

如果容器元素尚未成為網頁版面配置的一部分（例如，它可能使用`display:none`樣式隱藏），檢視器會暫停其初始化程式。 此專案會暫停，直到網頁將容器元素帶回版面配置時，檢視器載入會自動繼續。

在檢視器生命週期中僅呼叫此方法一次；後續呼叫會被忽略。

## 參數 {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

無。

## 傳回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}`檢視器執行個體的參考。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
