---
description: 傳送電子郵件給指定的收件者，以回應cdnCacheInvalidation作業。
solution: Experience Manager
title: 電子郵件確認
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: b4698637-a897-47fa-92d4-4ab400e56962
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 6%

---

# [!DNL EmailConfirmation]{#emailconfirmation}

傳送電子郵件給指定的收件者，以回應cdnCacheInvalidation作業。

語法

## 參數 {#section-490717fe96bf40c2a5a2f7ccbfaab3d0}

| 名稱 | 類型 | 說明 |
|---|---|---|
| 創作者 | `xsd:boolean` | 如果為true，則包含使用者的Web服務使用者帳戶，該帳戶為指定從Dynamic Media CDN接收電子郵件確認的電子郵件清單。 |
| ccOthersArray | `types:EmailArray` | 指定要從Dynamic Media CDN接收確認通知的電子郵件地址陣列（最多5個）。 |
