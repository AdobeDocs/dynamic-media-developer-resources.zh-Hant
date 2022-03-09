---
description: 作業運行後的作業日誌。
solution: Experience Manager
title: 作業日誌
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 80ae6669-6fe7-45a6-9a1d-f8544dd4f878
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 4%

---

# 作業日誌{#joblog}

作業運行後的作業日誌。

語法

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| 公司句柄 | `xsd:string` | 公司負責。 |
| 作業句柄 | `xsd:string` | 作業處理。 |
| 作業名稱 | `xsd:string` | 工作名稱. |
| 原始作業名 | `xsd:string` | 為作業提交的原始名稱 `submitJob`。 |
| 提交用戶電子郵件 | `xsd:string` | 提交作業的用戶的電子郵件地址。 |
| 日誌類型 | `xsd:string` | 作業日誌類型的選擇。 |
| jobSubType | `xsd:string` | 其他作業資訊。 |
| 開始日期 | `xsd:dateTime` | 作業的開始日期、時間和時區。 |
| 結束日期 | `xsd:dateTime` | 作業的結束日期、時間和時區。 |
| description | `xsd:string` | 最初在中指定的作業說明 `submitJob`。 |
| 檔案成功計數 | `xsd:int` | 成功處理的檔案數。 |
| fileErrorCount | `xsd:int` | 導致錯誤的檔案數。 |
| 檔案警告計數 | `xsd:int` | 生成警告的檔案數。 |
| fileDuplicateCount | `xsd:int` | 重複檔案數。 |
| 檔案更新計數 | `xsd:int` | 更新的檔案數。 |
| 總計檔案計數 | `xsd:int` | 已記錄作業處理的檔案數。 |
| transferSuccessCount | `xsd:int` | 成功傳輸的數量。 |
| transferErrorCount | `xsd:int` | 傳輸錯誤數。 |
| transferWarningCount | `xsd:int` | 傳輸警告數。 |
| 致命錯誤 | `xsd:boolean` | 作業是否生成致命錯誤。 |
| detailTotalRows | `xsd:int` | 與查詢匹配的行總數，其大小可能大於 `detailArray` 因為頁面大小限制。 |
| 詳細資訊陣列 | `types:JobLogDetailArray` | 有關已記錄作業的詳細資訊陣列。 |
