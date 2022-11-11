---
description: 階層式檔案或資產儲存物件。 資料夾可以包含一（或多個）子資料夾。
solution: Experience Manager
title: 檔案夾
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 74b44b1a-a92e-4c97-a93b-0cd4552f78ec
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 8%

---

# [!DNL Folder]{#folder}

階層式檔案或資產儲存物件。 資料夾可以包含一（或多個）子資料夾。

語法

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| folderHandle | `xsd:string` | 資料夾句柄。 |
| [!DNL path] | `xsd:string` | 資料夾路徑。 |
| lastModified | `xsd:dateTime` | 上次修改日期。 |
| childLastModified | `xsd:dateTime` | 子資料夾和資料夾子資產的上次修改日期。 |
| permissionsSetHandle | `xsd:string` | 資料夾權限處理。 |
| hasSubfolder | `types:Boolean` | 確定資料夾是否包含子資料夾。 |
| subfolderArray | `types:FolderArray` | 資料夾中的子資料夾陣列。 |
