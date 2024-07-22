---
title: init
description: 迴轉檢視器的JavaScript API參考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 5217a02a-6092-4cb9-b4fb-f959cdc85a6e
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 2%

---

# init{#init}

迴轉檢視器的JavaScript API參考。

`init()`

啟動迴轉檢視器的初始化。 此時必須建立容器`DOM`元素，檢視器程式碼才能依其ID找到它。

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
