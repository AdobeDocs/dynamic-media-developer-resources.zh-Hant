---
description: 包含與主作業日誌消息(JobDetail)關聯的補充消息。 包含與目前處理的資產相關的警告和其他詳細資料。
solution: Experience Manager
title: JobLogDetailAux
feature: Dynamic Media經典，SDK/API
role: 開發人員、管理員
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 6%

---


# JobLogDetailAux{#joblogdetailaux}

包含與主作業日誌消息(JobDetail)關聯的補充消息。 包含與目前處理的資產相關的警告和其他詳細資料。

語法

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| `*`logMessage`*` | `xsd:string` | 輔助資訊。 |
| `*`logType`*` | `xsd:string` | 日誌類型：`IPSJobLog.gcUploadWarning`或`IPSJobLog.gcUploadError`。 |
| `*`dateCreated`*` | `xsd:dateTime` | 輔助作業日誌建立日期。 |

