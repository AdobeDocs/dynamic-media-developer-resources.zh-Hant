---
description: 工作記錄檔資訊。
solution: Experience Manager
title: JobLogDetail
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fe41a48a-4671-4179-a128-aadc7bc0683b
TQID: 'https://experienceleague.adobe.com/wH0F5TxaTHxn-vP7PTri94WxEa5Bs9Q2-CRnuHdVb3I'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 60
ht-degree: 8%

---

# [!DNL JobLogDetail]{#joblogdetail}

工作記錄檔資訊。

語法

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| logMessage | `xsd:string` | 工作記錄檔中的訊息。 |
| logType | `xsd:string` | 工作記錄檔型別。 |
| assetName | `xsd:string` | 工作記錄檔中的資產名稱（選擇性）。 |
| assetType | `xsd:string` | 資產型別的選擇。 |
| assetHandle | `xsd:string` | 作業記錄中參照的資產控制代碼。 |
| auxArray | `types:JobLogDetailAuxArray` | 提供上述五種工作記錄型別以外的其他詳細工作記錄資訊。 |
