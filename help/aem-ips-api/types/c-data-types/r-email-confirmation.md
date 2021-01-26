---
description: 響應於cdnCacheInvalidation操作，將電子郵件傳送給指定的收件者。
solution: Experience Manager
title: 電子郵件確認
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 6%

---


# EmailConfirmation{#emailconfirmation}

響應於cdnCacheInvalidation操作，將電子郵件傳送給指定的收件者。

語法

## 參數 {#section-490717fe96bf40c2a5a2f7ccbfaab3d0}

| 名稱 | 類型 | 說明 |
|---|---|---|
| `*`ccOriginator`*` | `xsd:boolean` | 若為true，則包含使用者的web service使用者帳戶，此為指定接收來自Dynamic Media CDN之電子郵件確認的電子郵件清單。 |
| `*`ccOthersArray`*` | `types:EmailArray` | 一組電子郵件地址（最多5個），指定用來從Dynamic Media CDN接收確認通知。 |

