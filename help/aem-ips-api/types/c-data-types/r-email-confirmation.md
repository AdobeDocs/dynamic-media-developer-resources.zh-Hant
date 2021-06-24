---
description: 回應cdnCacheInvalidation操作，傳送電子郵件給指定的收件者。
solution: Experience Manager
title: EmailConfirmation
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: b4698637-a897-47fa-92d4-4ab400e56962
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 6%

---

# EmailConfirmation{#emailconfirmation}

回應cdnCacheInvalidation操作，傳送電子郵件給指定的收件者。

語法

## 參數 {#section-490717fe96bf40c2a5a2f7ccbfaab3d0}

| 名稱 | 類型 | 說明 |
|---|---|---|
| `*`ccOriginator`*` | `xsd:boolean` | 若為true，則包括使用者的網站服務使用者帳戶，此帳戶是指定用來接收來自Dynamic Media CDN之電子郵件確認的電子郵件清單。 |
| `*`ccOthersArray`*` | `types:EmailArray` | 一系列電子郵件地址（最多5個），指定用來接收來自Dynamic Media CDN的確認通知。 |
