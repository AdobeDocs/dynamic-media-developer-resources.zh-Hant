---
description: 更名資料夾。
seo-description: 更名資料夾。
seo-title: renameFolder
solution: Experience Manager
title: renameFolder
topic: Scene7 Image Production System API
uuid: 7d190a57-1d81-4f41-9205-b8ffdf7330ec
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# renameFolder{#renamefolder}

更名資料夾。

語法

## 授權使用者類型 {#section-5a252b00937d4befbec76fa23fbae9df}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>使用者必須擁有資產的讀取和寫入存取權。

## 參數 {#section-6fcee63dc3f74a5b90e1d71e59eb255c}

**輸入(renameFolderParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | 是 | 對包含要更名的資料夾的公司進行處理。 |
| ` *`folderHandle`*` | `xsd:string` | 是 | 資料夾的句柄。 |
| ` *`folderName`*` | `xsd:string` | 是 | 新資料夾名稱。 |

**輸出(renameFolderReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| ` *`folderHandle`*` | `xsd:string` | 是 | 已重新命名資料夾的控制代碼。 |

## 範例 {#section-98bdd2f88d164f488676e90aba1dc864}

此程式碼範例會重新命名資料夾。

**請求**

```java
<ns1:renameFolderParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:folderHandle>MyCompany/PDF/</ns1:folderHandle>
   <ns1:folderName>My Newly Renamed PDF Folder</ns1:folderName>
</ns1:renameFolderParam>
```

**回答**

```java
<renameFolderReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <folderHandle>MyCompany/My Newly Renamed PDF Folder/</folderHandle>
</renameFolderReturn>
```

