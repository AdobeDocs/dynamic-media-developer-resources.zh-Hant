---
description: 更新資料夾權限。
seo-description: 更新資料夾權限。
seo-title: updateFolderPermissions
solution: Experience Manager
title: updateFolderPermissions
topic: Scene7 Image Production System API
uuid: 940d7b63-80cf-4097-9cf9-8499b69181b7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# updateFolderPermissions{#updatefolderpermissions}

更新資料夾權限。

語法

## 授權使用者類型 {#section-e5c2217231bf4b3386e0ab3f2e9aca0b}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 參數 {#section-339e6e17c5504e1ea79fbdc05f618050}

**輸入(updateFolderPermissionsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | 是 | 公司負責人。 |
| ` *`folderHandle`*` | `xsd:string` | 是 | 資料夾句柄。 |
| ` *`updateChildren`*` | `xsd:boolean` | 是 | 確定是否使用為頂層資料夾設定的權限來更新子項。 |
| ` *`updateArray`*` | `types:PermissionUpdateArray` | 是 | 您要套用至資料夾的權限更新陣列。 |

**輸出(updateFolderPermissionsReturn)**

IPS API不會傳回此作業的回應。

## 範例 {#section-c3fe4d4388674870a3856c35ef66b631}

**請求**

```java
<ns1:updateFolderPermissionsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:folderHandle>MyCompany/eCatalogs/</ns1:folderHandle>
   <ns1:updateChildren>false</ns1:updateChildren>
   <ns1:updateArray>
      <ns1:items>
         <ns1:groupHandle>225</ns1:groupHandle>
         <ns1:permissionType>Read</ns1:permissionType>
         <ns1:isAllowed>true</ns1:isAllowed>
         <ns1:isOverride>true</ns1:isOverride>
      </ns1:items>
   </ns1:updateArray>
</ns1:updateFolderPermissionsParam>
```

**回答**

無。
