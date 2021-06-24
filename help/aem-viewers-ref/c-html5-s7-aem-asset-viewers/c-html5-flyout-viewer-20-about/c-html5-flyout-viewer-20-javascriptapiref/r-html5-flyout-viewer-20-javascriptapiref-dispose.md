---
description: 飛出檢視器的JavaScript API參考。
solution: Experience Manager
title: 處置
feature: Dynamic Media Classic，檢視器，SDK/API,Flyout
role: Developer,Business Practitioner
exl-id: bf38d481-d8cc-400c-9017-bcb3471f2a10
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 3%

---

# 處置{#dispose}

飛出檢視器的JavaScript API參考。

`dispose()`

釋出檢視器邏輯使用的所有資源，並刪除檢視器在執行階段建立的所有內部物件和元件，以處理此檢視器例項。

網頁程式碼也應刪除檢視器例項變數，才能從網頁瀏覽器記憶體中完全移除檢視器。

如果網頁代碼已直接在檢視器SDK元件上註冊事件監聽器（檢視器使用）或儲存的此類元件的外部引用（此類監聽器必須由網頁代碼顯式註冊），且在呼叫`dispose()`之前，必須刪除此類外部元件引用。

呼叫`dispose()`後，請勿再存取檢視器API。

## 參數 {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

無。

## 傳回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

無。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```
