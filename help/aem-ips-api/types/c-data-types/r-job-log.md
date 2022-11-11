---
description: 作業運行後的作業日誌。
solution: Experience Manager
title: 作業日誌
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 80ae6669-6fe7-45a6-9a1d-f8544dd4f878
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 3%

---

# [!DNL JobLog]{#joblog}

作業運行後的作業日誌。

語法

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| companyHandle | `xsd:string` | 公司負責人。 |
| jobHandle | `xsd:string` | 工作處理。 |
| jobName | `xsd:string` | 工作名稱. |
| originalJobName | `xsd:string` | 為具有的作業提交的原始名稱 `submitJob`. |
| submitUserEmail | `xsd:string` | 提交作業的使用者的電子郵件地址。 |
| logType | `xsd:string` | 作業日誌類型的選擇。 |
| jobSubType | `xsd:string` | 其他作業資訊。 |
| startDate | `xsd:dateTime` | 作業的開始日期、時間和時區。 |
| endDate | `xsd:dateTime` | 作業的結束日期、時間和時區。 |
| [!DNL description] | `xsd:string` | 作業的說明，如 `submitJob`. |
| fileSuccessCount | `xsd:int` | 已成功處理的檔案數。 |
| fileErrorCount | `xsd:int` | 導致錯誤的檔案數。 |
| fileWarningCount | `xsd:int` | 生成警告的檔案數。 |
| fileDuplicateCount | `xsd:int` | 重複檔案的數量。 |
| fileUpdateCount | `xsd:int` | 已更新的檔案數。 |
| totalFileCount | `xsd:int` | 記錄的作業處理的檔案數。 |
| transferSuccessCount | `xsd:int` | 成功傳輸的數量。 |
| transferErrorCount | `xsd:int` | 傳輸錯誤數。 |
| transferWarningCount | `xsd:int` | 傳輸警告數。 |
| fatalError | `xsd:boolean` | 作業是否產生致命錯誤。 |
| detailTotalRows | `xsd:int` | 符合查詢的總列數，可能大於 `detailArray` 因為頁面大小限制。 |
| detailArray | `types:JobLogDetailArray` | 記錄作業的詳細資訊陣列。 |
