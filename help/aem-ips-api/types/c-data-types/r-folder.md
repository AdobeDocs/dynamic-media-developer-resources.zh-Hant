---
description: 階層式檔案或資產儲存物件。 檔案夾可以包含一（或多個）子檔案夾。
solution: Experience Manager
title: 檔案夾
feature: Dynamic Media經典，SDK/API
role: 開發人員、管理員
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 10%

---


# 檔案夾{#folder}

階層式檔案或資產儲存物件。 檔案夾可以包含一（或多個）子檔案夾。

語法

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| `*`folderHandle`*` | `xsd:string` | 資料夾句柄。 |
| `*`路徑`*` | `xsd:string` | 資料夾路徑。 |
| `*`lastModified`*` | `xsd:dateTime` | 上次修改日期。 |
| `*`childLastModified`*` | `xsd:dateTime` | 子資料夾和資料夾子資產的上次修改日期。 |
| `*`permissionsSetHandle`*` | `xsd:string` | 資料夾權限控制代碼。 |
| `*`hasSubfolder`*` | `types:Boolean` | 確定資料夾是否包含子資料夾。 |
| `*`subfolderArray`*` | `types:FolderArray` | 資料夾中的子資料夾陣列。 |

