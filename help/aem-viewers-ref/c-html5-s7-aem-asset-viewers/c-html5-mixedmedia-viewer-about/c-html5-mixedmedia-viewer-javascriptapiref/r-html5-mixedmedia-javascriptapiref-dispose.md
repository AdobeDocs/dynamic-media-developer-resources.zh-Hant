---
description: 混合媒體檢視器的JavaScript API參考。
solution: Experience Manager
title: 處置
feature: Dynamic Media Classic,Viewers,SDK/API,Mix Media Sets
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 2%

---


# dispose{#dispose}

混合媒體檢視器的JavaScript API參考。

`dispose()`

借由釋放檢視器邏輯使用的所有資源，並刪除檢視器在執行時期中建立的所有內部物件和元件，來設定此檢視器例項。

網頁程式碼也應刪除檢視器例項變數，以便從網頁瀏覽器記憶體中完全移除檢視器。

如果網頁程式碼已直接在檢視器SDK元件上註冊事件偵聽器，檢視器會使用或儲存這些元件的外部參考，則這類監聽器必須由網頁程式碼明確取消註冊，而且這些外部元件參考必須在呼叫`dispose()`之前先刪除。

呼叫`dispose()`後，請勿再存取檢視器API。

## 參數 {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

無。

## 傳回{#section-1d3cf85bc7cc4dfe9670e038d02b9101}

無。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```

