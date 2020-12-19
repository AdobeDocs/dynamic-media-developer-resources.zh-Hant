---
description: 回轉檢視器的JavaScript API參考。
seo-description: 回轉檢視器的JavaScript API參考。
seo-title: init
solution: Experience Manager
title: init
topic: Dynamic media
uuid: 1803028f-dcba-49da-9fb7-78bfd64fc47d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 2%

---


# init{#init}

回轉檢視器的JavaScript API參考。

`init()`

啟動回轉檢視器的初始化。 此時，必須建立容器`DOM`元素，讓檢視器程式碼可依其ID找到它。

如果容器元素尚未成為網頁版面的一部分（例如，它可能會使用指派給它的`display:none`樣式隱藏），檢視器會暫停其初始化程式，直到網頁將容器元素帶回版面為止。 發生此情況時，檢視器載入會自動繼續。

在檢視器生命週期中，只需呼叫此方法一次；會忽略後續呼叫。

## 參數 {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

無。

## 傳回{#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` 檢視器例項的參考。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```

