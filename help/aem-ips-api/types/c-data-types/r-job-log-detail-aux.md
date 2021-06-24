---
description: 包含與主作業日誌消息(JobDetail)關聯的補充消息。 包含與目前處理的資產相關聯的警告和其他詳細資料。
solution: Experience Manager
title: JobLogDetailAux
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 789736c5-d74d-4970-9665-b43e316aca69
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 7%

---

# JobLogDetailAux{#joblogdetailaux}

包含與主作業日誌消息(JobDetail)關聯的補充消息。 包含與目前處理的資產相關聯的警告和其他詳細資料。

語法

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| `*`logMessage`*` | `xsd:string` | 輔助資訊。 |
| `*`logType`*` | `xsd:string` | 日誌類型：`IPSJobLog.gcUploadWarning`或`IPSJobLog.gcUploadError`。 |
| `*`dateCreated`*` | `xsd:dateTime` | 輔助作業日誌建立日期。 |
