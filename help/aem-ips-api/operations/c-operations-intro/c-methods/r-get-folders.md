---
description: 返回從資料夾路徑開始的所有資料夾和子資料夾。 getFolders響應最多返回100,000個資料夾。
solution: Experience Manager
title: getFolders
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 71fe3343-2560-4d74-8ec3-1229d83a62e1
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 8%

---

# getFolders{#getfolders}

返回從資料夾路徑開始的所有資料夾和子資料夾。 getFolders響應最多返回100,000個資料夾。

## 資料夾的用途 {#section-66e344d5333f42f1b060a0cba25935c3}

使用資料夾可以組織子資料夾和資產。 所有資料夾和資產名稱必須唯一。 共用相同名稱的資料夾和資產將導致命名空間衝突，即使它們位於不同的資料夾層次結構中。
語法

## 授權用戶類型 {#section-0dc7e17cb60f4cf7bcdb76648e5d2f8e}

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
>用戶必須具有對資料夾的讀取權限才能返回其上的資料。

## 參數 {#section-0c1976503eaa418a9226b51667901176}

**輸入(getFoldersParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 公司句柄 | `xsd:string` | 是 | 公司的把手。 |
| accessUserHandle | `xsd:string` | 否 | 管理員用於模擬特定用戶。 |
| accessGroupHandle | `xsd:string` | 否 | 按特定組篩選。 |
| 資料夾路徑 | `xsd:string` | 否 | 將資料夾和所有子資料夾檢索到葉級別的根資料夾。 如果排除，則使用公司根。 |
| assetTypeArray | `types:StringArray` | 否 | 返回僅包含指定資產類型的資料夾。 |
| 響應欄位陣列 | `types:StringArray` | 否 | 包含要包括在響應中的欄位清單。 |
| 排除欄位陣列 | `types:StringArray` | 否 | 包含要從響應中排除的欄位清單。 |

**輸出(getFoldersReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| folderArray | `types:FolderArray` | 否 | 符合篩選條件的資料夾陣列。 響應最多限制為100,000個資料夾。 |
| 權限SetArray | `types:PermissionSetArray` |  |  |

## 範例 {#section-b5cb06e9fb9945ad898dbdc3692b754e}

此代碼示例返回一個陣列，該陣列包含公司的所有資料夾以及每個資料夾的特定資訊。

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
