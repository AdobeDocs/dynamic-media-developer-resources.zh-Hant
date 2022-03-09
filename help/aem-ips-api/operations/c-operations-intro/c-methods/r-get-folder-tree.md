---
description: 返回分層樹結構中的資料夾和子資料夾。 getFolderTree響應最多限制為100,000個資料夾
solution: Experience Manager
title: getFolderTree
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1afe63ca-d11a-4fa5-a26b-90a23bee1b68
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 9%

---

# getFolderTree{#getfoldertree}

返回分層樹結構中的資料夾和子資料夾。 getFolderTree響應最多限制為100,000個資料夾

語法

## 授權用戶類型 {#section-66ef19149f4d4123a3a99004b5a2743e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>用戶必須具有對資料夾的讀取權限才能返回其上的資料。

## 參數 {#section-0c2b30513f1e439cbd840e8cc6465b3a}

**輸入(getFolderTreeParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 公司句柄 | `xsd:string` | 是 | 公司的把手。 |
| accessUserHandle | `xsd:string` | 否 | 僅由管理員用於模擬特定用戶。 |
| accessGroupHandle | `xsd:string` | 否 | 用於按特定組篩選，包括公司所屬的任何組。 |
| 資料夾路徑 | `xsd:string` | 否 | 將資料夾和所有子資料夾檢索到葉級別的根資料夾。 如果排除，則使用公司根。 |
| 深度 | `xsd:int` | 是 | 值為零將獲取頂級資料夾。 任何其它值都指定要下降到樹中的深度。 |
| assetTypeArray | `types:StringArray` | 否 | 返回僅包含指定資產類型的資料夾。 |
| 響應欄位陣列 | `types:StringArray` | 否 | 包含要包括在響應中的欄位清單。 |
| 排除欄位陣列 | `types:StringArray` | 否 | 包含要在響應中排除的欄位清單。 |

**輸出(getFolderTreeReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 資料夾 | `types:folders` | 否 | 樹結構中資料夾的層次結構。 響應最多限制為100,000個資料夾。 |
| 權限SetArray | `types:PermissionSetArray` |  |  |

## 範例 {#section-a9fd2edb56574dd9bf8b0f2fd89367e4}

此代碼示例使用公司句柄和深度參數來確定響應應返回的深度級別。 響應包含與相關的資料夾和子資料夾陣列。 將深度值設定為較小的數值，以在資料夾樹中進行更深入的搜索。

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
