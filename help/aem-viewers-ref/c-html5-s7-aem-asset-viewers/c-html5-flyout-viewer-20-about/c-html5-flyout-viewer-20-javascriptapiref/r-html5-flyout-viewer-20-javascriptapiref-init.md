---
description: 用於Flyout查看器的JavaScript API參考。
solution: Experience Manager
title: 初始化
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: e86f8c0f-c130-43c5-8c3a-07c6bc49e2f7
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 2%

---

# 初始化{#init}

用於Flyout查看器的JavaScript API參考。

`init()`

啟動浮出查看器的初始化。 此時，必須建立容器DOM元素，以便查看器代碼可以通過其ID找到它。

如果容器元素尚未成為網頁佈局的一部分(例如，可能會使用 `display:none` )，查看器將暫停其初始化過程，直到網頁將容器元素帶回佈局的那一刻。 出現這種情況時，查看器載入將自動恢復。

在查看器生命週期期間只應調用一次此方法，將忽略後續調用。

## 參數 {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

無。

## 返回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` 對查看器實例的引用。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
