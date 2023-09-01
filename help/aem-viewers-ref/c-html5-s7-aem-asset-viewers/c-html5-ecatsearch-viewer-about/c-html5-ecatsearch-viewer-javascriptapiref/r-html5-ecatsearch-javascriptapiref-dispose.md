---
title: 處置
description: eCatalog檢視器的JavaScript API參考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: fda6d50f-0e1b-436c-af2e-1ccc9cd51c39
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 3%

---

# 處置{#dispose}

eCatalog檢視器的JavaScript API參考。

[!DNL `dispose()`]

釋放檢視器邏輯使用的所有資源，並刪除檢視器在執行階段建立的所有內部物件和元件，以處置此檢視器執行個體。

網頁程式碼也應刪除檢視器例項變數，並從網頁瀏覽器記憶體中完全移除檢視器。

如果網頁程式碼已直接在檢視器所使用的Viewer SDK元件上註冊事件接聽程式，或已儲存此類元件的外部參照，則此類接聽程式必須由網頁程式碼明確取消註冊。 而且，在呼叫之前，必須刪除這類外部元件參考 [!DNL `dispose()`].

之後不要再存取檢視器API [!DNL `dispose()`] 稱為。

## 參數 {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

無。

## 傳回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

無。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```
