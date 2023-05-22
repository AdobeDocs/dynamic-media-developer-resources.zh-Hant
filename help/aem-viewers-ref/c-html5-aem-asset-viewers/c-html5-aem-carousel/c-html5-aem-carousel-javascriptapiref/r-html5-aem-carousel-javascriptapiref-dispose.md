---
title: 處置
description: Carousel查看器的JavaScript API參考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 64e9f83f-e17e-4544-825a-fd458e15fdb5
source-git-commit: 96ac67e5645c2c55920cc971806ba2f14ae57044
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 3%

---

# 處置{#dispose}

Carousel查看器的JavaScript API參考。

`dispose()`

通過釋放查看器邏輯使用的所有資源並刪除運行時查看器建立的所有內部對象和元件來處置此查看器實例。

網頁代碼還應刪除查看器實例變數，以便從Web瀏覽器記憶體中完全刪除查看器。

如果網頁代碼已直接在查看器SDK元件上註冊事件偵聽器，或者已儲存了對此類元件的外部引用，則此類偵聽器必須由網頁代碼顯式註銷。 而且，在調用前必須刪除此類外部元件引用 `dispose()`。

以後不再訪問查看器API `dispose()` 。

## 參數 {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

無。

## 返回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

無。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```
