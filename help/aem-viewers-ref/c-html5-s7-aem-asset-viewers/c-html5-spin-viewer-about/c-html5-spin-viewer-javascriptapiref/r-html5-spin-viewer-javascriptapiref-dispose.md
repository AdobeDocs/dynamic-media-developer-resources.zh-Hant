---
title: 處置
description: 迴轉檢視器的JavaScript API參考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: c19466a8-9fc5-440c-8bb1-c4528937a522
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 3%

---

# 處置{#dispose}

迴轉檢視器的JavaScript API參考。

`dispose()`

釋放檢視器邏輯使用的所有資源，並在執行階段刪除檢視器建立的所有內部物件和元件，以處置此檢視器執行個體。

網頁程式碼也應刪除檢視器例項變數，並從網頁瀏覽器記憶體中完全移除檢視器。

如果網頁程式碼已直接在檢視器使用的Viewer SDK元件上註冊事件接聽程式（或已儲存對此類元件的外部參考），則此類接聽程式必須由網頁程式碼明確取消註冊。 而且，在呼叫之前，必須刪除此類外部元件參考 `dispose()`.

之後不再存取檢視器API `dispose()` 稱為。

## 參數 {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

無。

## 傳回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

無。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```
