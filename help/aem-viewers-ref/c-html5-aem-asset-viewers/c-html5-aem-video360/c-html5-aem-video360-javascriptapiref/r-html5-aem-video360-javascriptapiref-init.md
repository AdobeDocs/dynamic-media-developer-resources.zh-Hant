---
title: init
description: Video360檢視器的JavaScript API參考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: cb543620-e774-407b-bf33-bfd2261511c4
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 2%

---

# init{#init}

Video360檢視器的JavaScript API參考。

`init()`

啟動Video360查看器的初始化。 此時必須建立容器DOM元素，檢視器程式碼才能透過其ID找到它。

如果容器元素尚未成為網頁版面的一部分（例如，可能會使用指派給它的`display:none`樣式來隱藏），檢視器會暫停其初始化程式。 直到網頁將容器元素帶回版面為止。 發生此事件時，檢視器載入會自動繼續。

在檢視器生命週期期間，只需呼叫此方法一次；會忽略後續呼叫。

## 參數 {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

無。

## 傳回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` 檢視器例項的參考。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
