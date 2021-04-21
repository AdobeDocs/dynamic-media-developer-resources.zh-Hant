---
description: 傳回階層式樹狀結構中的檔案夾和子檔案夾。 getFolderTree回應的限制為最多100,000個資料夾
solution: Experience Manager
title: getFolderTree
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 9%

---


# getFolderTree{#getfoldertree}

傳回階層式樹狀結構中的檔案夾和子檔案夾。 getFolderTree回應的限制為最多100,000個資料夾

語法

## 授權用戶類型{#section-66ef19149f4d4123a3a99004b5a2743e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>使用者必須擁有資料夾的讀取存取權，才能傳回資料夾上的資料。

## 參數 {#section-0c2b30513f1e439cbd840e8cc6465b3a}

**輸入(getFolderTreeParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 公司的把手。 |
| `*`accessUserHandle`*` | `xsd:string` | 否 | 僅供管理員用來模擬特定使用者。 |
| `*`accessGroupHandle`*` | `xsd:string` | 否 | 用於依特定群組篩選，包括公司所屬的任何群組。 |
| `*`folderPath`*` | `xsd:string` | 否 | 根資料夾，用於將資料夾和所有子資料夾檢索到葉層。 如果排除，則會使用公司根目錄。 |
| `*`深度`*` | `xsd:int` | 是 | 值零會取得頂層資料夾。 任何其它值都指定要下降到樹中的深度。 |
| `*`assetTypeArray`*` | `types:StringArray` | 否 | 傳回僅包含指定資產類型的檔案夾。 |
| `*`responseFieldArray`*` | `types:StringArray` | 否 | 包含要包含在回應中的欄位清單。 |
| `*`excludeFieldArray`*` | `types:StringArray` | 否 | 包含您要在回應中排除的欄位清單。 |

**輸出(getFolderTreeReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`資料夾`*` | `types:folders` | 否 | 樹結構中資料夾的層次。 回應上限為100,000個資料夾。 |
| `*`permissionSetArray`*` | `types:PermissionSetArray` |  |  |

## 範例 {#section-a9fd2edb56574dd9bf8b0f2fd89367e4}

此程式碼範例使用公司控制代碼和深度參數來判斷回應應傳回的深度等級。 響應包含具有相關的資料夾和子資料夾陣列。 將深度值設定為較小的數字，以便在資料夾樹中進行更深入的搜索。

**請求**

```java
<ns1:getFolderTreeParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:depth>-1</ns1:depth>
</ns1:getFolderTreeParam>
```

**回答**

```java
<getFolderTreeReturn xmlns="http://www.scene7.com/IpsApi/xsd/">
  <folders>
    <items>
      <folderHandle>f|sampleFolder/uploadTestDir/</folderHandle>
      <path>MyCompany/uploadTestDir/</path>
      <lastModified>2011-11-14T11:19:59.031-08:00</lastModified>
      <childLastModified>2011-11-14T11:19:59.031-08:00</childLastModified>
      <permissionSetHandle>pm|2</permissionSetHandle>
      <hasSubfolders>true</hasSubfolders>
      <subfolderArray>
        <items>
          <folderHandle>f|MyCompany/uploadTestDir/SubFolder/</folderHandle>
          <path>DevanCo/uploadTestDir/SubFolder/</path>
          <lastModified>2011-11-14T11:19:59.032-08:00</lastModified>
          <childLastModified>2011-11-14T11:19:59.032-08:00</childLastModified>
          <permissionSetHandle>pm|2</permissionSetHandle>
          <hasSubfolders>true</hasSubfolders>
          <subfolderArray>
            <items>
              <folderHandle>f|MyCompany/uploadTestDir/SubFolder/10/</folderHandle>
              <path>DevanCo/uploadTestDir/SubFolder/10/</path>
              <lastModified>2011-11-14T11:19:59.033-08:00</lastModified>
              <childLastModified>2011-11-14T15:06:58.563-08:00</childLastModified>
              <permissionSetHandle>pm|2</permissionSetHandle>
              <hasSubfolders>false</hasSubfolders>
            </items>
          </subfolderArray>
        </items>
      </subfolderArray>
    </items>
  </folders>
  <permissionSetArray>
    <items>
      <permissionSetHandle>pm|2</permissionSetHandle>
      <permissionArray>
        <items>
          <groupHandle>g|1</groupHandle>
          <groupName>Asset Download Group</groupName>
          <permissionType>Read</permissionType>
          <isAllowed>true</isAllowed>
          <isOverride>false</isOverride>
        </items>
        <items>
          <groupHandle>g|2</groupHandle>
          <groupName>Asset Upload Group</groupName>
          <permissionType>Read</permissionType>
          <isAllowed>true</isAllowed>
          <isOverride>true</isOverride>
        </items>
        <items>
          <groupHandle>g|2</groupHandle>
          <groupName>Asset Upload Group</groupName>
          <permissionType>Write</permissionType>
          <isAllowed>true</isAllowed>
          <isOverride>true</isOverride>
        </items>
      </permissionArray>
    </items>
  <permissionSetArray>
</getFolderTreeReturn>
```

