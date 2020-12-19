---
description: 包含與主作業日誌消息(JobDetail)關聯的補充消息。 包含與目前處理的資產相關的警告和其他詳細資料。
seo-description: 包含與主作業日誌消息(JobDetail)關聯的補充消息。 包含與目前處理的資產相關的警告和其他詳細資料。
seo-title: JobLogDetailAux
solution: Experience Manager
title: JobLogDetailAux
topic: Scene7 Image Production System API
uuid: df6f61f2-54f1-4996-938c-c3ea8c27551a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 5%

---


# JobLogDetailAux{#joblogdetailaux}

包含與主作業日誌消息(JobDetail)關聯的補充消息。 包含與目前處理的資產相關的警告和其他詳細資料。

語法

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| ` *`logMessage`*` | `xsd:string` | 輔助資訊。 |
| ` *`logType`*` | `xsd:string` | 日誌類型：`IPSJobLog.gcUploadWarning`或`IPSJobLog.gcUploadError`。 |
| ` *`dateCreated`*` | `xsd:dateTime` | 輔助作業日誌建立日期。 |

