---
title: init
description: 智慧型裁切視訊檢視器的JavaScript API參考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: e197c4dd-346d-4ef4-beb7-cbd0049dff05
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 2%

---

# init{#init}

智慧型裁切視訊檢視器的JavaScript API參考。

`init()`

開始初始化智慧型裁切視訊檢視器。 此時，必須建立容器DOM元素，讓檢視器程式碼可依其ID尋找。

如果容器元素尚未成為網頁版面配置的一部分（例如，可能使用指派給它的`display:none`樣式將其隱藏），檢視器會暫停其初始化程式。 直到網頁將容器元素帶回版面配置為止。 當此動作發生時，檢視器載入會自動繼續。

在檢視器生命週期中僅呼叫此方法一次；後續呼叫會被忽略。

## 參數 {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

無。

## 傳回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}`檢視器執行個體的參考。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
