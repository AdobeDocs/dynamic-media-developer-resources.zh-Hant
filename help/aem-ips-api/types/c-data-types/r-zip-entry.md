---
description: ZIP檔案中的一個專案。
solution: Experience Manager
title: ZipEntry
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f71f57db-6717-4a27-b275-19bc4cf59ea4
TQID: 'https://experienceleague.adobe.com/u8w7i9pPiCJTkbxwQXg-IBIz3hDWtxrEvqNJ5JERM64'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 70c478ebbe0b38d9e35c1bb26074a458c0197b2b
workflow-type: tm+mt
source-wordcount: 42
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

