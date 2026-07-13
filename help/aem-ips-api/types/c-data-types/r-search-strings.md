---
description: 從PDF檔案擷取的搜尋字串記錄。
solution: Experience Manager
title: SearchStrings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 3f67ba8a-12dd-4698-9502-7cbdec9cb25d
TQID: 'https://experienceleague.adobe.com/bWokSVoIEkxrKgXAkaR4ycgSjZAWb2trFnqokTe98XQ'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 83717f155466c1b33cab6f1f8830a9fea68c88c5
workflow-type: tm+mt
source-wordcount: 81
ht-degree: 12%

---

# [!DNL SearchStrings]{#searchstrings}

從PDF檔案擷取的搜尋字串記錄。

語法

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| searchString | `xsd:string` | 搜尋字串文字。 |
| 關鍵字陣列 | `types:KeywordsArray` | 搜尋字串中的關鍵字陣列。 |
| 狀態 | `xsd:boolean` | 如果搜尋字串有效且已啟用，則為True。 |
| x | `xsd:int` | 搜尋字串的X軸位置。 |
| y | `xsd:int` | 搜尋字串的Y軸位置。 |
| 寬度 | `xsd:int` | 搜尋字串寬度。 |
| 高度 | `xsd:int` | 搜尋字串高度。 |
| 字型名稱 | `xsd:string` | 搜尋字串中使用的字型名稱。 |
| pointSize | `xsd:string` | 字型大小。 |

