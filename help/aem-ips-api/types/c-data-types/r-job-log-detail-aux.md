---
description: 包含與主要工作記錄檔訊息(JobDetail)相關聯的補充訊息。 包含警告和與目前處理資產相關聯的其他詳細資訊。
solution: Experience Manager
title: 工作記錄詳細資訊
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 789736c5-d74d-4970-9665-b43e316aca69
TQID: 'https://experienceleague.adobe.com/Hl3L69Hd6Hm8acRaPgFVQCfo8PffGCn5fNGxthmStFM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 83717f155466c1b33cab6f1f8830a9fea68c88c5
workflow-type: tm+mt
source-wordcount: 64
ht-degree: 7%

---

# [!DNL JobLogDetailAux]{#joblogdetailaux}

包含與主要工作記錄檔訊息(JobDetail)相關聯的補充訊息。 包含警告和與目前處理資產相關聯的其他詳細資訊。

語法

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| logMessage | `xsd:string` | 輔助訊息。 |
| logType | `xsd:string` | 記錄型別： `IPSJobLog.gcUploadWarning`或`IPSJobLog.gcUploadError`。 |
| 日期已建立 | `xsd:dateTime` | 輔助工作記錄檔建立日期。 |

