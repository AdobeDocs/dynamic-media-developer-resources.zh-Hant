---
description: 從資料夾路徑開始，返回所有資料夾和子資料夾。 getFolders回應最多會傳回100,000個資料夾。
solution: Experience Manager
title: getFolders
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 71fe3343-2560-4d74-8ec3-1229d83a62e1
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '242'
ht-degree: 8%

---

# getFolders{#getfolders}

從資料夾路徑開始，返回所有資料夾和子資料夾。 getFolders回應最多會傳回100,000個資料夾。

## 資料夾的用途 {#section-66e344d5333f42f1b060a0cba25935c3}

資料夾可讓您組織子資料夾和資產。 所有資料夾和資產名稱必須是唯一的。 共用相同名稱的資料夾和資產會造成命名空間衝突，即使它們位於不同的資料夾階層亦然。
語法

## 授權的使用者類型 {#section-0dc7e17cb60f4cf7bcdb76648e5d2f8e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>使用者必須擁有資料夾的讀取存取權，才能傳回資料夾上的資料。

## 參數 {#section-0c1976503eaa418a9226b51667901176}

**輸入(getFoldersParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 公司的把手。 |
| `*`accessUserHandle`*` | `xsd:string` | 否 | 由管理員用來模擬特定使用者。 |
| `*`accessGroupHandle`*` | `xsd:string` | 否 | 依特定群組篩選。 |
| `*`folderPath`*` | `xsd:string` | 否 | 用於檢索資料夾和葉級所有子資料夾的根資料夾。 如果排除，則會使用公司根。 |
| `*`assetTypeArray`*` | `types:StringArray` | 否 | 傳回僅包含指定資產類型的資料夾。 |
| `*`responseFieldArray`*` | `types:StringArray` | 否 | 包含您要納入回應的欄位清單。 |
| `*`excludeFieldArray`*` | `types:StringArray` | 否 | 包含要從回應中排除的欄位清單。 |

**輸出(getFoldersReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`folderArray`*` | `types:FolderArray` | 否 | 符合篩選條件的資料夾陣列。 回應最多限制為100,000個資料夾。 |
| `*`permissionsSetArray`*` | `types:PermissionSetArray` |  |  |

## 範例 {#section-b5cb06e9fb9945ad898dbdc3692b754e}

此程式碼範例會傳回一個陣列，其中包含公司的所有資料夾，以及每個資料夾的特定資訊。

**請求**

```java
<ns1:getFoldersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getFoldersParam>
```

**回答**

```java
<getFoldersReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <folderArray>
      <items>
         <folderHandle>MyCompany/</folderHandle>
         <path>MyCompany/</path>
         <hasSubfolders>false</hasSubfolders>
      </items>
      <items>
         <folderHandle>MyCompany/eCatalogs/</folderHandle>
         <path>MyCompany/eCatalogs/</path>
         <hasSubfolders>false</hasSubfolders>
      </items>
      <items>
         <folderHandle>MyCompany/PDF/</folderHandle>
         <path>MyCompany/PDF/</path>
         <hasSubfolders>false</hasSubfolders>
      </items>
   </folderArray>
</getFoldersReturn>
```
