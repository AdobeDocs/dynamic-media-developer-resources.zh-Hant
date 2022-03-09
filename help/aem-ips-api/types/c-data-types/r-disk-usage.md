---
description: 資產或資料夾的磁碟空間統計資訊。
solution: Experience Manager
title: 磁碟使用
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: a3c4c1cd-0fcc-4e7a-a4aa-884d0ce2f208
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '51'
ht-degree: 13%

---

# 磁碟使用{#diskusage}

資產或資料夾的磁碟空間統計資訊。

語法

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| 公司句柄 | `xsd:string` | 公司負責。 |
| 公司名稱 | `xsd:string` | 公司名稱. |
| imageCount | `xsd:int` | 儲存的影像數。 |
| 磁碟空間用法 | `xsd:long` | 檔案端總數(KB)。 |
| 上次修改時間 | `xsd:dateTime` | 日期、時間和時區 `DiskUsage` 類型上次修改時間。 |
