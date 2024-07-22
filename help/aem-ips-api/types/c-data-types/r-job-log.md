---
description: 工作執行後的工作記錄。
solution: Experience Manager
title: 工作記錄檔
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 80ae6669-6fe7-45a6-9a1d-f8544dd4f878
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 2%

---

# [!DNL JobLog]{#joblog}

工作執行後的工作記錄。

語法

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| companyHandle | `xsd:string` | 公司控制代碼。 |
| jobHandle | `xsd:string` | 工作控制代碼。 |
| jobName | `xsd:string` | 工作名稱。 |
| 原始工作名稱 | `xsd:string` | 為具有`submitJob`的工作提交的原始名稱。 |
| submitUserEmail | `xsd:string` | 提交工作之使用者的電子郵件地址。 |
| logType | `xsd:string` | 選擇工作記錄型別。 |
| 工作子型別 | `xsd:string` | 其他工作資訊。 |
| startDate | `xsd:dateTime` | 工作的開始日期、時間和時區。 |
| endDate | `xsd:dateTime` | 工作的結束日期、時間和時區。 |
| [!DNL description] | `xsd:string` | `submitJob`中最初指定的工作描述。 |
| fileSuccessCount | `xsd:int` | 已成功處理的檔案數。 |
| fileErrorCount | `xsd:int` | 導致錯誤的檔案數。 |
| fileWarningCount | `xsd:int` | 產生警告的檔案數。 |
| fileDuplicateCount | `xsd:int` | 重複檔案的數量。 |
| fileUpdateCount | `xsd:int` | 已更新的檔案數。 |
| totalfilecount | `xsd:int` | 記錄的工作處理的檔案數。 |
| transferSuccessCount | `xsd:int` | 成功的傳輸數目。 |
| Transferrorcount | `xsd:int` | 傳輸錯誤數。 |
| transferWarningCount | `xsd:int` | 傳輸警告的數目。 |
| fatalError | `xsd:boolean` | 工作是否產生嚴重錯誤。 |
| detailTotalRows | `xsd:int` | 符合查詢的資料列總數，由於頁面大小限制，可能會大於`detailArray`的大小。 |
| detailArray | `types:JobLogDetailArray` | 有關記錄工作的詳細資訊陣列。 |
