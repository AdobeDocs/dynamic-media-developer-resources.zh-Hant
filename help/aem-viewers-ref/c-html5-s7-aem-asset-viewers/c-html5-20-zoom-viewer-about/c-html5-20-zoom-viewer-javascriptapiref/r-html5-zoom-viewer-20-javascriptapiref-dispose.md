---
title: 處置
description: 縮放檢視器的JavaScript API參考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: c796943e-8ea8-4a97-a1ff-09676204150a
TQID: 'https://experienceleague.adobe.com/Fi7inW4o2cQ5r3518sL7n8GWCJZeVf94Za4-2unBzRE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: f6432244ef9faba7a81488e9de8e438154ae6123
workflow-type: tm+mt
source-wordcount: 124
ht-degree: 3%

---

# 處置{#dispose}

縮放檢視器的JavaScript API參考。

`dispose()`

釋放檢視器邏輯使用的所有資源，並刪除檢視器在執行階段建立的所有內部物件和元件，以處置此檢視器執行個體。

網頁程式碼也應刪除檢視器例項變數，並從網頁瀏覽器記憶體中完全移除檢視器。

如果網頁程式碼已直接在檢視器所使用的Viewer SDK元件上註冊事件接聽程式，或已儲存對此類元件的外部參考，則此類接聽程式必須由網頁程式碼明確取消註冊。 而且，在呼叫`dispose()`之前，必須先刪除這類外部元件參考。

呼叫`dispose()`後，不要再存取檢視器API。

## 參數 {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

無。

## 傳回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

無。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```

