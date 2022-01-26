---
title: 初始化
description: 用於混合媒體查看器的JavaScript API參考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 4fb40cec-172a-41b3-98fc-927da88c7cb9
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 2%

---

# 初始化{#init}

用於混合媒體查看器的JavaScript API參考。

`init()`

啟動混合媒體查看器的初始化。 此時，必須建立容器DOM元素，以便查看器代碼可以通過其ID找到它。

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
