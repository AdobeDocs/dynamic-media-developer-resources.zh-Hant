---
description: ZIP檔案中的一個專案。
solution: Experience Manager
title: ZipEntry
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f71f57db-6717-4a27-b275-19bc4cf59ea4
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '42'
ht-degree: 14%

---

# [!DNL ZipEntry]{#zipentry}

ZIP檔案中的一個專案。

語法

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| name | `xsd:string` | 專案名稱。 |
| isDirectory | `xsd:boolean` | 決定專案是否為目錄。 |
| lastModified | `xsd:dateTime` | 上次修改的日期和時間。 |
| compressedSize | `xsd:long` | 壓縮大小。 |
| uncompressedSize | `xsd:long` | 未壓縮的大小。 |
