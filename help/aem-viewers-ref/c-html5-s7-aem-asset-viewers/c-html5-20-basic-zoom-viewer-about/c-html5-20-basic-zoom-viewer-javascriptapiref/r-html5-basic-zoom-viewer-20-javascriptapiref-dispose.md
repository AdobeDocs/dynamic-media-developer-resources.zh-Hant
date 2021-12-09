---
title: 處置
description: 基本縮放檢視器的JavaScript API參考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 49c353f7-deab-43a7-84dd-21fda7864574
source-git-commit: 61e3a1fd0e21d336eaf5232096f5b1b54f2a6353
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 3%

---

# 處置{#dispose}

基本縮放檢視器的JavaScript API參考。

`dispose()`

釋出檢視器邏輯使用的所有資源，並刪除檢視器在執行階段建立的所有內部物件和元件，以處理此檢視器例項。

網頁程式碼也應刪除檢視器例項變數，才能從網頁瀏覽器記憶體中完全移除檢視器。

如果網頁代碼已直接在檢視器使用的檢視器SDK元件上註冊事件監聽器（或儲存此類元件的外部引用），則此類監聽器必須由網頁代碼顯式註銷。 而且，在呼叫之前，必須刪除此類外部元件參考 `dispose()`.

在 `dispose()` 的URL。

## 參數 {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

無。

## 傳回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

無。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```
