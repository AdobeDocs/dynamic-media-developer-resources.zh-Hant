---
description: 返回所有資料夾和子資料夾，從資料夾路徑開始。 getFolders回應最多會傳回100,000個資料夾。
solution: Experience Manager
title: getFolders
feature: Dynamic Media經典，SDK/API
role: 開發人員、管理員
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 8%

---


# getFolders{#getfolders}

返回所有資料夾和子資料夾，從資料夾路徑開始。 getFolders回應最多會傳回100,000個資料夾。

## 資料夾{#section-66e344d5333f42f1b060a0cba25935c3}的用途

檔案夾可讓您組織子檔案夾和資產。 所有資料夾和資產名稱都必須是唯一的。 共用相同名稱的資料夾和資產會造成命名空間衝突，即使它們位於不同的資料夾階層。
語法

## 授權用戶類型{#section-0dc7e17cb60f4cf7bcdb76648e5d2f8e}

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
| `*`accessUserHandle`*` | `xsd:string` | 否 | 管理員用來模擬特定使用者。 |
| `*`accessGroupHandle`*` | `xsd:string` | 否 | 依特定群組篩選。 |
| `*`folderPath`*` | `xsd:string` | 否 | 根資料夾，用於將資料夾和所有子資料夾檢索到葉層。 如果排除，則會使用公司根目錄。 |
| `*`assetTypeArray`*` | `types:StringArray` | 否 | 傳回僅包含指定資產類型的檔案夾。 |
| `*`responseFieldArray`*` | `types:StringArray` | 否 | 包含要包含在回應中的欄位清單。 |
| `*`excludeFieldArray`*` | `types:StringArray` | 否 | 包含要從回應中排除的欄位清單。 |

**輸出(getFoldersReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`folderArray`*` | `types:FolderArray` | 否 | 符合篩選條件的資料夾陣列。 響應限制為最多100,000個資料夾。 |
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

