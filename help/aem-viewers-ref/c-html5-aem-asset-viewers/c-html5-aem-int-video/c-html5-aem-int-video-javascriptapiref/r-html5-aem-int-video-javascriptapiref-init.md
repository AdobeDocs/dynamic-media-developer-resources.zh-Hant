---
title: 初始化
description: Interactive Video Viewer的JavaScript API參考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 5fcc7dcd-a9a8-4a87-9c8d-42717ced8ae9
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 2%

---

# 初始化{#init}

Interactive Video Viewer的JavaScript API參考。

`init()`

啟動互動式視頻查看器的初始化。 此時，必須建立容器DOM元素，以便查看器代碼可以通過其ID找到它。

如果容器元素尚未成為網頁佈局的一部分，則可能會使用 `display:none` 樣式 — 查看器將暫停其初始化過程。 直到網頁將容器元素帶回佈局為止。 發生此事件時，查看器載入將自動恢復。

在查看器生命週期中僅調用此方法一次；將忽略後續調用。

## 參數 {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

無。

## 返回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` 對查看器實例的引用。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
