---
description: Video360檢視器的JavaScript API參考。
seo-description: Video360檢視器的JavaScript API參考。
seo-title: 處置
solution: Experience Manager
title: 處置
uuid: bdecadb1-4e77-43d5-9da5-80e5101efb36
feature: Dynamic Media經典，檢視器，SDK/API,360 VR視訊
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 2%

---


# dispose{#dispose}

Video360檢視器的JavaScript API參考。

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

