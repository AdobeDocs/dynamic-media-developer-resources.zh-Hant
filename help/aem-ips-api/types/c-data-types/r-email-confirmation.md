---
description: 響應cdnCacheInvalidation操作向指定收件人發送電子郵件。
solution: Experience Manager
title: 電子郵件確認
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: b4698637-a897-47fa-92d4-4ab400e56962
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 6%

---

# 電子郵件確認{#emailconfirmation}

響應cdnCacheInvalidation操作向指定收件人發送電子郵件。

語法

## 參數 {#section-490717fe96bf40c2a5a2f7ccbfaab3d0}

| 名稱 | 類型 | 說明 |
|---|---|---|
| ccOriginator | `xsd:boolean` | 如果為true，則包括用戶的Web服務用戶帳戶，該帳戶是指定從Dynamic MediaCDN接收電子郵件確認的電子郵件清單。 |
| 其他陣列 | `types:EmailArray` | 指定從Dynamic MediaCDN接收確認通知的電子郵件地址陣列（最多5個）。 |
