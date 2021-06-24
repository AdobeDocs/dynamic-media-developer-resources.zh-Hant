---
description: 互動式視訊檢視器的JavaScript API參考。
solution: Experience Manager
title: 處置
feature: Dynamic Media Classic，檢視器， SDK/API，互動式影片
role: Developer,Business Practitioner
exl-id: 55418b97-3d18-4c1d-b0e3-aefd71f46616
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 2%

---

# 處置{#dispose}

互動式視訊檢視器的JavaScript API參考。

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
