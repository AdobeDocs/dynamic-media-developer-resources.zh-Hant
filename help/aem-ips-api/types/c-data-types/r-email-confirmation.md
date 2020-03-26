---
description: 響應於cdnCacheInvalidation操作，將電子郵件傳送給指定的收件者。
seo-description: 響應於cdnCacheInvalidation操作，將電子郵件傳送給指定的收件者。
seo-title: 電子郵件確認
solution: Experience Manager
title: 電子郵件確認
topic: Scene7 Image Production System API
uuid: c3b7aada-a03a-418d-80b2-31a86a1af786
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 電子郵件確認{#emailconfirmation}

響應於cdnCacheInvalidation操作，將電子郵件傳送給指定的收件者。

語法

## 參數 {#section-490717fe96bf40c2a5a2f7ccbfaab3d0}

| 名稱 | 類型 | 說明 |
|---|---|---|
| ` *`ccOriginator`*` | `xsd:boolean` | 若為true，則包含使用者的web service使用者帳戶，此為指定接收Scene7 CDN電子郵件確認的電子郵件清單。 |
| ` *`ccOthersArray`*` | `types:EmailArray` | 一組電子郵件地址（最多5個），指定用來接收來自Scene7 CDN的確認通知。 |

