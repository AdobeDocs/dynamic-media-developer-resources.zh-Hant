---
description: 資產或資料夾的磁碟空間統計資訊。
solution: Experience Manager
title: DiskUsage
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: a3c4c1cd-0fcc-4e7a-a4aa-884d0ce2f208
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 12%

---

# DiskUsage{#diskusage}

資產或資料夾的磁碟空間統計資訊。

語法

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 公司負責人。 |
| `*`companyName`*` | `xsd:string` | 公司名稱. |
| `*`imageCount`*` | `xsd:int` | 儲存的影像數。 |
| `*`diskSpaceUsage`*` | `xsd:long` | 檔案端總計（千位元組）。 |
| `*`lastModified`*` | `xsd:dateTime` | 上次修改`DiskUsage`類型的日期、時間和時區。 |
