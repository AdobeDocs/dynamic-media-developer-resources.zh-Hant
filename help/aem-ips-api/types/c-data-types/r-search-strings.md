---
description: 從PDF檔案中擷取搜尋字串記錄。
solution: Experience Manager
title: SearchStrings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 3f67ba8a-12dd-4698-9502-7cbdec9cb25d
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 14%

---

# [!DNL SearchStrings]{#searchstrings}

從PDF檔案中擷取搜尋字串記錄。

語法

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| searchString | `xsd:string` | 搜尋字串文字。 |
| keywordsArray | `types:KeywordsArray` | 搜尋字串中的關鍵字陣列。 |
| 狀態 | `xsd:boolean` | 如果搜索字串有效且已啟用，則返回true。 |
| x | `xsd:int` | 搜尋字串的X軸位置。 |
| y | `xsd:int` | 搜索字串的Y軸位置。 |
| 寬度 | `xsd:int` | 搜尋字串寬度。 |
| 高度 | `xsd:int` | 搜尋字串高度。 |
| fontName | `xsd:string` | 搜索字串中使用的字型名稱。 |
| pointSize | `xsd:string` | 字型大小. |
