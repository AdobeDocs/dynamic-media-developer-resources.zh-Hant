---
title: init
description: 適用於彈出式檢視器初始化的JavaScript API參考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: e86f8c0f-c130-43c5-8c3a-07c6bc49e2f7
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 2%

---

# init{#init}

彈出式檢視器的JavaScript API參考。

`init()`

開始初始化彈出式檢視器。 此時，必須建立容器DOM元素，讓檢視器程式碼可依其ID尋找。

例如，如果容器元素尚未成為網頁版面配置的一部分，則可以使用指派給它的`display:none`樣式將其隱藏，檢視器會暫停其初始化程式。 直到網頁將容器元素帶回版面配置為止。 發生此情況時，檢視器會自動繼續載入。

在檢視器生命週期中只應呼叫一次此方法，後續呼叫會被忽略。

## 參數 {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

無。

## 傳回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}`檢視器執行個體的參考。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
