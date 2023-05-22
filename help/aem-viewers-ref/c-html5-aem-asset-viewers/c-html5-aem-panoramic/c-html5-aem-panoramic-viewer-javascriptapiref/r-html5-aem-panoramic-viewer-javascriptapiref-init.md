---
title: 初始化
description: 用於Panoramic Viewer的JavaScript API參考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
exl-id: cb543620-e774-407b-bf33-bfd2261511c4
source-git-commit: 8aebcacd5abdc23565aab1bc3506c36f055b6439
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 2%

---

# 初始化{#init}

用於Panoramic Viewer的JavaScript API參考。

`init()`

啟動全景查看器的初始化。 此時，必須建立容器DOM元素，以便查看器代碼可以通過其ID找到它。

如果容器元素尚未成為網頁佈局的一部分(例如，它可能已使用 `display:none` 樣式)，查看器將掛起其初始化過程。 直到網頁將容器元素帶回佈局為止。 發生此事件時，查看器載入將自動恢復。

在查看器生命週期期間只應調用一次此方法，隨後的調用將被忽略。

## 參數 {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

無。

## 返回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` 對查看器實例的引用。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
