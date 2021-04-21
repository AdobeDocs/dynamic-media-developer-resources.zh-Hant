---
description: 使用權限資產來設定單一資產的權限。
solution: Experience Manager
title: setAssetPermissions
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 8%

---


# setAssetPermissions{#setassetpermissions}

使用權限資產來設定單一資產的權限。

資產預設會繼承其父資料夾的權限。 一旦您設定資產的權限，除非您呼叫`removeAssetPermissions`，否則資產不會再繼承其父項的權限。

## 授權用戶類型{#section-91fafc170c734ed2a77beafda9221768}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 參數 {#section-e05abbce6453450fb38747101cb5e228}

**輸入(setAssetPermissonsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 包含您要使用之資料夾之公司的控制代碼。 |
| `*`assetHandle`*` | `xsd:string` | 是 | 資料夾句柄。 |
| `*`permissionArray`*` | `types:PermissionsUpdateArray` | 是 | 權限陣列。 |

**輸出(setAssetPermissonsReturn)**

IPS API不會傳回此作業的回應。

## 範例 {#section-38955bc330bb4909b6b06027ef2b143e}

此程式碼範例會設定資產的權限。 它包含公司和資產控制代碼，以及權限陣列。

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
