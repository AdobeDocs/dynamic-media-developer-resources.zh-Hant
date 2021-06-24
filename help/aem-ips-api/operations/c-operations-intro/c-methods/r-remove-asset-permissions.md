---
description: 從選取的資產移除權限。
solution: Experience Manager
title: removeAssetPermissions
feature: Dynamic Media Classic,SDK/API，資產管理
role: Developer,Administrator
exl-id: c47d9853-91b1-45fe-b8ff-aaa1239ca0d1
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 16%

---

# removeAssetPermissions{#removeassetpermissions}

從選取的資產移除權限。

語法

## 授權的使用者類型 {#section-239058fdb4454e519ac327e621cb3abc}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 參數 {#section-b70bf3b033ca45b396964baf2ab1fb0f}

**輸入(removeAssetPermissionsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 公司的把手。 |
| `*`assetHandle`*` | `xsd:string` | 是 | 具有您要移除之權限的資產控制代碼。 |

**輸出(removeAssetPermissionsReturn)**

IPS API不會針對此操作傳回回應。

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
