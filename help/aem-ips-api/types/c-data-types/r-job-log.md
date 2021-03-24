---
description: 作業運行後的作業日誌。
solution: Experience Manager
title: JobLog
feature: Dynamic Media經典，SDK/API
role: 開發人員、管理員
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 3%

---


# JobLog{#joblog}

作業運行後的作業日誌。

語法

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 公司負責人。 |
| `*`jobHandle`*` | `xsd:string` | 工作代理。 |
| `*`jobName`*` | `xsd:string` | 工作名稱. |
| `*`originalJobName`*` | `xsd:string` | 為具有`submitJob`的作業提交的原始名稱。 |
| `*`submitUserEmail`*` | `xsd:string` | 提交工作之使用者的電子郵件地址。 |
| `*`logType`*` | `xsd:string` | 作業日誌類型選擇。 |
| `*`jobSubType`*` | `xsd:string` | 其他工作資訊。 |
| `*`startDate`*` | `xsd:dateTime` | 作業的開始日期、時間和時區。 |
| `*`endDate`*` | `xsd:dateTime` | 作業的結束日期、時間和時區。 |
| `*`描述`*` | `xsd:string` | `submitJob`中最初指定的作業說明。 |
| `*`fileSuccessCount`*` | `xsd:int` | 成功處理的檔案數。 |
| `*`fileErrorCount`*` | `xsd:int` | 導致錯誤的檔案數。 |
| `*`fileWarningCount`*` | `xsd:int` | 產生警告的檔案數。 |
| `*`fileDuplicateCount`*` | `xsd:int` | 重複檔案的數目。 |
| `*`fileUpdateCount`*` | `xsd:int` | 已更新的檔案數。 |
| `*`totalFileCount`*` | `xsd:int` | 記錄作業處理的檔案數。 |
| `*`transferSuccessCount`*` | `xsd:int` | 成功傳輸的數量。 |
| `*`transferErrorCount`*` | `xsd:int` | 傳輸錯誤數。 |
| `*`transferWarningCount`*` | `xsd:int` | 傳輸警告數。 |
| `*`fatalError`*` | `xsd:boolean` | 作業是否生成致命錯誤。 |
| `*`detailTotalRows`*` | `xsd:int` | 符合查詢的總行數，由於頁面大小限制，該總行數可能大於`detailArray`的大小。 |
| `*`detailArray`*` | `types:JobLogDetailArray` | 記錄作業的詳細資訊陣列。 |

