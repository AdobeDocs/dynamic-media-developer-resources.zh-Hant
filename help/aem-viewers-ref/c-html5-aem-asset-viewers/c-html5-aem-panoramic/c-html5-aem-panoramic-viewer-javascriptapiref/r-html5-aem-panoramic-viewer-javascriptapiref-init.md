---
title: init
description: 全景檢視器的JavaScript API參考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
exl-id: cb543620-e774-407b-bf33-bfd2261511c4
source-git-commit: 8aebcacd5abdc23565aab1bc3506c36f055b6439
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 2%

---

# init{#init}

全景檢視器的JavaScript API參考。

`init()`

啟動全景查看器的初始化。 此時必須建立容器DOM元素，檢視器程式碼才能透過其ID找到它。

如果容器元素尚未成為網頁版面的一部分(例如，可能會使用 `display:none` 樣式)，檢視器會暫停其初始化程式。 直到網頁將容器元素帶回版面為止。 發生此事件時，檢視器載入會自動繼續。

在檢視器生命週期期間，此方法只應呼叫一次，後續的呼叫會遭到忽略。

## 參數 {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

無。

## 傳回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` 檢視器例項的參考。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
