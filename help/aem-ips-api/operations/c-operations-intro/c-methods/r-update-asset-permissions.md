---
description: 更新資產權限。
solution: Experience Manager
title: updateAssetPermissons
feature: Dynamic Media Classic,SDK/API，資產管理
role: Developer,Administrator
exl-id: 12972a52-7b70-405c-9c73-e5ce6ab7dd9b
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 21%

---

# updateAssetPermissons{#updateassetpermissons}

更新資產權限。

語法

## 授權的使用者類型 {#section-3928e9badc3842e1859af4ed362df719}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 參數 {#section-392cb3076cf84790a32fd913f2b111a3}

**輸入(updateAssetPermissionsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 公司負責人。 |
| `*`assetHandle`*` | `xsd:string` | 是 | 資產控制代碼。 |
| `*`updateArray`*` | `types:PermissionUpdateArray` | 是 | 您要套用至資產的權限。 |

**輸出(updateAssetPermissionsReturn)**

IPS API不會針對此操作傳回回應。

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
