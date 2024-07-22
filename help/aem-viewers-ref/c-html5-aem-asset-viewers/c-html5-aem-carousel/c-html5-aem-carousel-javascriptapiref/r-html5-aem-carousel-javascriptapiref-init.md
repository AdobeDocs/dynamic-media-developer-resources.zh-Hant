---
title: init
description: 轉盤檢視器的JavaScript API參考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 00e09e26-1380-487c-9512-34d805f1330d
source-git-commit: 96ac67e5645c2c55920cc971806ba2f14ae57044
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 2%

---

# init{#init}

轉盤檢視器的JavaScript API參考。

`init()`

開始初始化轉盤檢視器。 此時，必須建立容器DOM元素，讓檢視器程式碼可依其ID尋找。

如果容器元素尚未成為網頁版面配置的一部分（例如，它可能使用`display:none`樣式隱藏），檢視器會暫停其初始化程式。 此專案會暫停，直到網頁將容器元素帶回版面配置時，檢視器載入會自動繼續。

在檢視器生命週期中僅呼叫此方法一次；後續呼叫會被忽略。

## 參數 {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

無。

## 傳回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}`檢視器執行個體的參考。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
