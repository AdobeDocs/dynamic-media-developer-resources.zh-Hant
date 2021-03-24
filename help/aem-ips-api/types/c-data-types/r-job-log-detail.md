---
description: 作業日誌資訊。
solution: Experience Manager
title: JobLogDetail
feature: Dynamic Media經典，SDK/API
role: 開發人員、管理員
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 7%

---


# JobLogDetail{#joblogdetail}

作業日誌資訊。

語法

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| `*`logMessage`*` | `xsd:string` | 作業日誌中的消息。 |
| `*`logType`*` | `xsd:string` | 作業日誌檔案類型。 |
| `*`assetName`*` | `xsd:string` | 作業記錄檔中的資產名稱（選用）。 |
| `*`assetType`*` | `xsd:string` | 資產類型選擇。 |
| `*`assetHandle`*` | `xsd:string` | 作業日誌中引用的資產句柄。 |
| `*`auxArray`*` | `types:JobLogDetailAuxArray` | 提供上述五種作業日誌類型以外的其他詳細作業日誌資訊。 |

