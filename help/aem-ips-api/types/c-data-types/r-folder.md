---
description: 分層檔案或資產儲存對象。 資料夾可以包含一個（或多個）子資料夾。
solution: Experience Manager
title: 檔案夾
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 74b44b1a-a92e-4c97-a93b-0cd4552f78ec
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 11%

---

# 檔案夾{#folder}

分層檔案或資產儲存對象。 資料夾可以包含一個（或多個）子資料夾。

語法

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| folderHandle | `xsd:string` | 資料夾句柄。 |
| 路徑 | `xsd:string` | 資料夾路徑。 |
| 上次修改時間 | `xsd:dateTime` | 上次修改日期。 |
| 子上次修改時間 | `xsd:dateTime` | 子資料夾和資料夾子資產的上次修改日期。 |
| 權限SetHandle | `xsd:string` | 資料夾權限句柄。 |
| 有子資料夾 | `types:Boolean` | 確定資料夾是否包含子資料夾。 |
| 子資料夾陣列 | `types:FolderArray` | 資料夾中的子資料夾陣列。 |
