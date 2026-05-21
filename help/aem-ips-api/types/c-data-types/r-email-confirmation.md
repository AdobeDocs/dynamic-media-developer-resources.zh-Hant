---
description: 傳送電子郵件給指定的收件者，以回應cdnCacheInvalidation作業。
solution: Experience Manager
title: 電子郵件確認
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: b4698637-a897-47fa-92d4-4ab400e56962
TQID: 'https://experienceleague.adobe.com/h9ZZRR0zR347mzSifomCmtNW5GorTC6fgGjeSRf52KU'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 78
ht-degree: 6%

---

# [!DNL EmailConfirmation]{#emailconfirmation}

傳送電子郵件給指定的收件者，以回應cdnCacheInvalidation作業。

語法

## 參數 {#section-490717fe96bf40c2a5a2f7ccbfaab3d0}

| 名稱 | 類型 | 說明 |
|---|---|---|
| 創作者 | `xsd:boolean` | 如果為true，則包含使用者的Web服務使用者帳戶，該帳戶為指定接收來自Dynamic Media CDN的電子郵件確認的電子郵件清單。 |
| ccOthersArray | `types:EmailArray` | 指定要從Dynamic Media CDN接收確認通知的電子郵件地址陣列（最多5個）。 |
