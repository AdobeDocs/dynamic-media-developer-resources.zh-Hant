---
description: 從選定資產中刪除權限。
solution: Experience Manager
title: removeAssetPermissions
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: c47d9853-91b1-45fe-b8ff-aaa1239ca0d1
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 17%

---

# removeAssetPermissions{#removeassetpermissions}

從選定資產中刪除權限。

語法

## 授權用戶類型 {#section-239058fdb4454e519ac327e621cb3abc}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 參數 {#section-b70bf3b033ca45b396964baf2ab1fb0f}

**輸入(removeAssetPermissionsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 公司句柄 | `xsd:string` | 是 | 公司的把手。 |
| 資產句柄 | `xsd:string` | 是 | 具有要刪除的權限的資產的句柄。 |

**輸出(removeAssetPermissionsReturn)**

IPS API不會為此操作返迴響應。

## 範例 {#section-238fa7bb091548f5ba72ced11fc92d4f}

此代碼示例從資產中刪除權限。

**請求**

```java
<ns1:removeAssetPermissionsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>15674|25|1062</ns1:assetHandle>
</ns1:removeAssetPermissionsParam>
```

**回答**

無。
