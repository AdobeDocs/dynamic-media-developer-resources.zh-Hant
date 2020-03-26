---
description: 互動式視訊檢視器的JavaScript API參考。
seo-description: 互動式視訊檢視器的JavaScript API參考。
seo-title: init
solution: Experience Manager
title: init
topic: Dynamic media
uuid: e6ec0730-1ddc-4026-939c-2c9f8ecee5c7
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7

---


# init{#init}

互動式視訊檢視器的JavaScript API參考。

`init()`

啟動Interactive Video Viewer的初始化。 目前，必須建立容器DOM元素，讓檢視器程式碼可依其ID找到它。

如果容器元素尚未成為網頁版面的一部分（例如，可能會使用指派給它的樣式來隱藏它），檢視器會暫停其初始化程式，直到網頁將容器元素帶回版面為止。 `display:none` 發生此情況時，檢視器載入會自動繼續。

在檢視器生命週期中，只需呼叫此方法一次；會忽略後續呼叫。

## 參數 {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

無。

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` 檢視器例項的參考。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```

