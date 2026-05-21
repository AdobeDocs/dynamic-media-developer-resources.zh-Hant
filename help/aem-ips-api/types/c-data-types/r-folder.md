---
description: 階層檔案或資產儲存物件。 資料夾可以包含一個（或多個）子資料夾。
solution: Experience Manager
title: 檔案夾
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 74b44b1a-a92e-4c97-a93b-0cd4552f78ec
TQID: 'https://experienceleague.adobe.com/nh6zqOnt-bxAFmsHSHPRCMThKlOwi-9b9fep6ujKZyE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 70
ht-degree: 8%

---

# [!DNL Folder]{#folder}

階層檔案或資產儲存物件。 資料夾可以包含一個（或多個）子資料夾。

語法

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| folderHandle | `xsd:string` | 資料夾控制代碼。 |
| [!DNL path] | `xsd:string` | 資料夾路徑。 |
| lastModified | `xsd:dateTime` | 上次修改日期。 |
| childLastModified | `xsd:dateTime` | 子資料夾和資料夾子資產的上次修改日期。 |
| permissionsSetHandle | `xsd:string` | 檔案夾許可權控制代碼。 |
| hasSubfolder | `types:Boolean` | 決定資料夾是否有子資料夾。 |
| subfolderarray | `types:FolderArray` | 資料夾中的子資料夾陣列。 |
