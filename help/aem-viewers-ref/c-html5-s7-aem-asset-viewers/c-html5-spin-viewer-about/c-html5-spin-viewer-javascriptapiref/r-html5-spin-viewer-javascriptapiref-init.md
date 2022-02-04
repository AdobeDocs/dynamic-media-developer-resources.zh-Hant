---
title: 初始化
description: 用於Spin Viewer的JavaScript API參考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 5217a02a-6092-4cb9-b4fb-f959cdc85a6e
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 2%

---

# 初始化{#init}

用於Spin Viewer的JavaScript API參考。

`init()`

啟動旋轉查看器的初始化。 到這時，容器 `DOM` 必須建立元素，以便查看器代碼可以通過其ID找到它。

如果容器元素尚未成為網頁佈局的一部分，則可能會使用 `display:none` 樣式 — 查看器暫停其初始化過程。 它被掛起，直到網頁將容器元素帶回佈局的那一刻，此時查看器載入將自動恢復。

在查看器生命週期中僅調用此方法一次；將忽略後續調用。

## 參數 {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

無。

## 返回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` 對查看器實例的引用。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
