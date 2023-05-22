---
description: 包含與主作業日誌消息(JobDetail)關聯的補充消息。 包括警告和與當前處理的資產關聯的其他詳細資訊。
solution: Experience Manager
title: 作業日誌詳細資訊輔助
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 789736c5-d74d-4970-9665-b43e316aca69
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 7%

---

# [!DNL JobLogDetailAux]{#joblogdetailaux}

包含與主作業日誌消息(JobDetail)關聯的補充消息。 包括警告和與當前處理的資產關聯的其他詳細資訊。

語法

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| 日誌消息 | `xsd:string` | 輔助資訊。 |
| 日誌類型 | `xsd:string` | 日誌類型： `IPSJobLog.gcUploadWarning` 或 `IPSJobLog.gcUploadError`。 |
| 建立日期 | `xsd:dateTime` | 輔助作業日誌建立日期。 |
