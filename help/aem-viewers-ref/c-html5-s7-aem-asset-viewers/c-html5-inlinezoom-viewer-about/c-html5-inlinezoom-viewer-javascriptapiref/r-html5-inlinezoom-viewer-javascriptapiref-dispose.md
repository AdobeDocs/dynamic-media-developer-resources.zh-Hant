---
title: 處置
description: 內嵌縮放檢視器的JavaScript API參考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 7e525bc1-6986-414c-acc0-e011dfd7b84b
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 3%

---

# 處置{#dispose}

內嵌縮放檢視器的JavaScript API參考。

`dispose()`

釋放檢視器邏輯使用的所有資源，並刪除檢視器在執行階段建立的所有內部物件和元件，以處置此檢視器執行個體。

網頁程式碼也應刪除檢視器例項變數，並從網頁瀏覽器記憶體中完全移除檢視器。

如果網頁程式碼已直接在檢視器使用的Viewer SDK元件上註冊事件接聽程式，或已儲存對這些元件的外部參考，則此類接聽程式必須由網頁程式碼明確取消註冊。 而且，在呼叫`dispose()`之前，必須先刪除這類外部元件參考。

呼叫`dispose()`後，不要再存取檢視器API。

## 參數 {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

無。

## 傳回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

無。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```
