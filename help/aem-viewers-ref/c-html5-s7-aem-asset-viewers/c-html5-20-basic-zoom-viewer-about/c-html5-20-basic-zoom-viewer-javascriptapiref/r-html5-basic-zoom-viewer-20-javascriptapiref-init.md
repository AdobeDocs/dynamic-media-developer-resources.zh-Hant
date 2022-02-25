---
title: 初始化
description: 用於基本縮放查看器的JavaScript API參考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: cef585ae-44d7-406c-96f9-e03959a8e518
source-git-commit: 61e3a1fd0e21d336eaf5232096f5b1b54f2a6353
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 2%

---

# 初始化{#init}

用於基本縮放查看器的JavaScript API參考。

`init()`

啟動基本縮放查看器的初始化。 此時，必須建立容器DOM元素，以便查看器代碼可以通過其ID找到它。

如果容器元素尚未成為網頁佈局的一部分(例如，它可能已使用 `display:none` 樣式)，查看器將掛起其初始化過程。 直到網頁將容器元素帶回佈局為止。 當此操作發生時，查看器將自動恢復載入。

在查看器生命週期中僅調用此方法一次；將忽略後續調用。

## 參數 {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

無。

## 返回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` 對查看器實例的引用。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
