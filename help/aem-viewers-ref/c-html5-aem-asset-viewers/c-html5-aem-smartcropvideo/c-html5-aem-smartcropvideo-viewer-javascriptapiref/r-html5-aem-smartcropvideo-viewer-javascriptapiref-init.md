---
title: 初始化
description: 用於Smart Crop Video Viewer的JavaScript API參考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: e197c4dd-346d-4ef4-beb7-cbd0049dff05
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 2%

---

# 初始化{#init}

用於Smart Crop Video Viewer的JavaScript API參考。

`init()`

啟動智慧裁剪視頻查看器的初始化。 此時，必須建立容器DOM元素，以便查看器代碼可以通過其ID找到它。

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
