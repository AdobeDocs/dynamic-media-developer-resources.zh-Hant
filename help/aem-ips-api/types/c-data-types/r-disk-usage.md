---
description: 資產或資料夾的磁碟空間統計資訊。
seo-description: 資產或資料夾的磁碟空間統計資訊。
seo-title: DiskUsage
solution: Experience Manager
title: DiskUsage
topic: Dynamic Media Image Production System API
uuid: a63f0ed0-c689-43b0-9c3e-9500715d15a5
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 11%

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
| `*`diskSpaceUsage`*` | `xsd:long` | 檔案端總計（以KB為單位）。 |
| `*`lastModified`*` | `xsd:dateTime` | 上次修改`DiskUsage`類型的日期、時間和時區。 |

