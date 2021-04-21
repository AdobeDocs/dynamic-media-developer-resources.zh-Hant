---
description: 響應於cdnCacheInvalidation操作，將電子郵件傳送給指定的收件者。
solution: Experience Manager
title: 電子郵件確認
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 5%

---


# EmailConfirmation{#emailconfirmation}

響應於cdnCacheInvalidation操作，將電子郵件傳送給指定的收件者。

語法

## 參數 {#section-490717fe96bf40c2a5a2f7ccbfaab3d0}

| 名稱 | 類型 | 說明 |
|---|---|---|
| `*`ccOriginator`*` | `xsd:boolean` | 若為true，則包含使用者的web service使用者帳戶，此為指定接收Dynamic MediaCDN電子郵件確認的電子郵件清單。 |
| `*`ccOthersArray`*` | `types:EmailArray` | 一組電子郵件地址（最多5個），指定用來接收來自Dynamic MediaCDN的確認通知。 |

