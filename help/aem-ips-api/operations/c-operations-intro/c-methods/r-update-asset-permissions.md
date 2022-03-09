---
description: 更新資產權限。
solution: Experience Manager
title: 更新資產權限
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 12972a52-7b70-405c-9c73-e5ce6ab7dd9b
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '54'
ht-degree: 24%

---

# 更新資產權限{#updateassetpermissons}

更新資產權限。

語法

## 授權用戶類型 {#section-3928e9badc3842e1859af4ed362df719}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 參數 {#section-392cb3076cf84790a32fd913f2b111a3}

**輸入(updateAssetPermissionsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 公司句柄 | `xsd:string` | 是 | 公司負責。 |
| 資產句柄 | `xsd:string` | 是 | 資產句柄。 |
| 更新陣列 | `types:PermissionUpdateArray` | 是 | 要應用到資產的權限。 |

**輸出(updateAssetPermissionsReturn)**

IPS API不會為此操作返迴響應。

## 範例 {#section-1b7b7dbfdab34c819a53f3d33004e1f9}

**請求**

```java
<ns1:updateAssetPermissionsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>15674|25|1062</ns1:assetHandle>
   <ns1:updateArray>
      <ns1:items>
         <ns1:groupHandle>225</ns1:groupHandle>
         <ns1:permissionType>Read</ns1:permissionType>
         <ns1:isAllowed>true</ns1:isAllowed>
         <ns1:isOverride>false</ns1:isOverride>
      </ns1:items>
   </ns1:updateArray>
</ns1:updateAssetPermissionsParam>
```

**回答**

無。
