---
description: 使用權限資產設定單一資產的權限。
solution: Experience Manager
title: setAssetPermissions
feature: Dynamic Media Classic,SDK/API，資產管理
role: Developer,Administrator
exl-id: 1e73c305-cda5-4c30-9380-ec4cd8309933
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 9%

---

# setAssetPermissions{#setassetpermissions}

使用權限資產設定單一資產的權限。

資產預設會繼承其父資料夾的權限。 一旦您對資產設定權限，除非您呼叫`removeAssetPermissions`，否則資產不再繼承其父項的權限。

## 授權的使用者類型 {#section-91fafc170c734ed2a77beafda9221768}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 參數 {#section-e05abbce6453450fb38747101cb5e228}

**輸入(setAssetPermissonsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 包含您要使用的資料夾的公司控制代碼。 |
| `*`assetHandle`*` | `xsd:string` | 是 | 資料夾句柄。 |
| `*`permissionArray`*` | `types:PermissionsUpdateArray` | 是 | 權限陣列。 |

**輸出(setAssetPermissonsReturn)**

IPS API不會針對此操作傳回回應。

## 範例 {#section-38955bc330bb4909b6b06027ef2b143e}

此程式碼範例會設定資產的權限。 其中包含公司和資產控制代碼，以及權限陣列。

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
