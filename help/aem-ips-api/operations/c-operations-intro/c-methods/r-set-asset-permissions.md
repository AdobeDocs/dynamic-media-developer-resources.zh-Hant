---
description: 使用權限資產設定單個資產的權限。
solution: Experience Manager
title: setAssetPermissions
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 1e73c305-cda5-4c30-9380-ec4cd8309933
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 9%

---

# setAssetPermissions{#setassetpermissions}

使用權限資產設定單個資產的權限。

預設情況下，資產繼承其父資料夾的權限。 一旦設定了對資產的權限，它就不再繼承其父項的權限，除非您調用 `removeAssetPermissions`。

## 授權用戶類型 {#section-91fafc170c734ed2a77beafda9221768}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 參數 {#section-e05abbce6453450fb38747101cb5e228}

**輸入(setAssetPermissonsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 公司句柄 | `xsd:string` | 是 | 包含要使用的資料夾的公司的句柄。 |
| 資產句柄 | `xsd:string` | 是 | 資料夾句柄。 |
| 權限陣列 | `types:PermissionsUpdateArray` | 是 | 權限陣列。 |

**輸出(setAssetPermissonsReturn)**

IPS API不會為此操作返迴響應。

## 範例 {#section-38955bc330bb4909b6b06027ef2b143e}

此代碼示例設定資產權限。 它包含公司和資產句柄以及權限陣列。

**請求**

```java
<setAssetPermissionsParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>64</companyHandle>
   <assetHandle>97374|1|61046</assetHandle>
   <permissionArray>
      <items>
         <groupHandle>521</groupHandle>
         <permissionType>Read</permissionType>
         <isAllowed>true</isAllowed>
         <isOverride>true</isOverride>
      </items>
   </permissionArray>
</setAssetPermissionsParam>
```

**回答**

無。
