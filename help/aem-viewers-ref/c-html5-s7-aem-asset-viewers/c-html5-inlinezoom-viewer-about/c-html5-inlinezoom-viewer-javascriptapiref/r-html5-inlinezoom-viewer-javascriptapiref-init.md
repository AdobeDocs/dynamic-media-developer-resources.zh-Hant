---
title: 初始化
description: 內聯縮放查看器的JavaScript API參考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: c4419728-1e1a-4e11-88fe-24eb0c968c5c
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 2%

---

# 初始化{#init}

內聯縮放查看器的JavaScript API參考。

`init()`

啟動查看器的初始化，以便查看器代碼可以通過其ID找到它。 此時必須建立容器DOM元素。

如果容器元素尚未成為網頁佈局的一部分，則可能會使用 `display:none` 樣式 — 查看器將暫停其初始化過程。 直到網頁將容器元素帶回佈局為止。 當此操作發生時，查看器載入將自動恢復。

在查看器生命週期中僅調用此方法一次；將忽略後續調用。

## 參數 {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

無。

## 返回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` 對查看器實例的引用。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
