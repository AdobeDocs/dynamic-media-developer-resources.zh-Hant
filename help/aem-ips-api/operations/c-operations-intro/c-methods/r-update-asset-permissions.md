---
description: 更新資產權限。
seo-description: 更新資產權限。
seo-title: updateAssetPermissons
solution: Experience Manager
title: updateAssetPermissons
topic: Scene7 Image Production System API
uuid: feb2faf3-81de-436e-82de-1e41df03508f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '58'
ht-degree: 22%

---


# updateAssetPermissons{#updateassetpermissons}

更新資產權限。

語法

## 授權用戶類型{#section-3928e9badc3842e1859af4ed362df719}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 參數 {#section-392cb3076cf84790a32fd913f2b111a3}

**輸入(updateAssetPermissionsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | 是 | 公司負責人。 |
| ` *`assetHandle`*` | `xsd:string` | 是 | 資產控制代碼。 |
| ` *`updateArray`*` | `types:PermissionUpdateArray` | 是 | 您要套用至資產的權限。 |

**輸出(updateAssetPermissionsReturn)**

IPS API不會傳回此作業的回應。

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
