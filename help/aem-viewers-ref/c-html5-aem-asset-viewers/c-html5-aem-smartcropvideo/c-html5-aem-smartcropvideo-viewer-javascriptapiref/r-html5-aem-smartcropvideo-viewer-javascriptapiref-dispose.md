---
title: 處置
description: 智慧型裁切視訊檢視器的JavaScript API參考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: c4bcccdc-6f23-4213-a1d1-03c5c62ba484
source-git-commit: b6ebc938f55117c4144ff921bed7f8742cf3a8a7
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 3%

---

# 處置{#dispose}

智慧型裁切視訊檢視器的JavaScript API參考。

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
