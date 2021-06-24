---
description: 作業運行後的作業日誌。
solution: Experience Manager
title: 作業日誌
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 80ae6669-6fe7-45a6-9a1d-f8544dd4f878
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 3%

---

# 作業日誌{#joblog}

作業運行後的作業日誌。

語法

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 公司負責人。 |
| `*`jobHandle`*` | `xsd:string` | 工作處理。 |
| `*`jobName`*` | `xsd:string` | 工作名稱. |
| `*`originalJobName`*` | `xsd:string` | 為`submitJob`作業提交的原始名稱。 |
| `*`submitUserEmail`*` | `xsd:string` | 提交作業的使用者的電子郵件地址。 |
| `*`logType`*` | `xsd:string` | 作業日誌類型的選擇。 |
| `*`jobSubType`*` | `xsd:string` | 其他作業資訊。 |
| `*`startDate`*` | `xsd:dateTime` | 作業的開始日期、時間和時區。 |
| `*`endDate`*` | `xsd:dateTime` | 作業的結束日期、時間和時區。 |
| `*`說明`*` | `xsd:string` | 最初在`submitJob`中指定的作業的說明。 |
| `*`fileSuccessCount`*` | `xsd:int` | 已成功處理的檔案數。 |
| `*`fileErrorCount`*` | `xsd:int` | 導致錯誤的檔案數。 |
| `*`fileWarningCount`*` | `xsd:int` | 生成警告的檔案數。 |
| `*`fileDuplicateCount`*` | `xsd:int` | 重複檔案的數量。 |
| `*`fileUpdateCount`*` | `xsd:int` | 已更新的檔案數。 |
| `*`totalFileCount`*` | `xsd:int` | 記錄的作業處理的檔案數。 |
| `*`transferSuccessCount`*` | `xsd:int` | 成功傳輸的數量。 |
| `*`transferErrorCount`*` | `xsd:int` | 傳輸錯誤數。 |
| `*`transferWarningCount`*` | `xsd:int` | 傳輸警告數。 |
| `*`fatalError`*` | `xsd:boolean` | 作業是否產生致命錯誤。 |
| `*`detailTotalRows`*` | `xsd:int` | 符合查詢的總列數，由於頁面大小限制，其大小可能大於`detailArray`。 |
| `*`detailArray`*` | `types:JobLogDetailArray` | 記錄作業的詳細資訊陣列。 |
