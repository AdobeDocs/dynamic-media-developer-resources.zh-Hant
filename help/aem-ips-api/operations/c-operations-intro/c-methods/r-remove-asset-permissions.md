---
description: 移除選取資產的權限。
seo-description: 移除選取資產的權限。
seo-title: removeAssetPermissions
solution: Experience Manager
title: removeAssetPermissions
topic: Scene7 Image Production System API
uuid: 5a351862-f412-4d89-90b7-9e70a26eacbc
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# removeAssetPermissions{#removeassetpermissions}

移除選取資產的權限。

語法

## 授權使用者類型 {#section-239058fdb4454e519ac327e621cb3abc}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 參數 {#section-b70bf3b033ca45b396964baf2ab1fb0f}

**輸入(removeAssetPermissionsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | 是 | 公司的把手。 |
| ` *`assetHandle`*` | `xsd:string` | 是 | 具有您要移除之權限的資產的控制代碼。 |

**輸出(removeAssetPermissionsReturn)**

IPS API不會傳回此作業的回應。

## 範例 {#section-238fa7bb091548f5ba72ced11fc92d4f}

此程式碼範例會移除資產的權限。

**請求**

```java
<ns1:removeAssetPermissionsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>15674|25|1062</ns1:assetHandle>
</ns1:removeAssetPermissionsParam>
```

**回答**

無。
