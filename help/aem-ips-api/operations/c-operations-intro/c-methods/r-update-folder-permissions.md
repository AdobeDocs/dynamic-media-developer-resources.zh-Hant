---
description: 更新資料夾權限。
solution: Experience Manager
title: updateFolderPermissions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 4e4f382e-4339-4b9d-a721-d33a4fa8be6b
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 19%

---

# updateFolderPermissions{#updatefolderpermissions}

更新資料夾權限。

語法

## 授權用戶類型 {#section-e5c2217231bf4b3386e0ab3f2e9aca0b}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 參數 {#section-339e6e17c5504e1ea79fbdc05f618050}

**輸入(updateFolderPermissionsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 公司句柄 | `xsd:string` | 是 | 公司負責。 |
| folderHandle | `xsd:string` | 是 | 資料夾句柄。 |
| 更新子項 | `xsd:boolean` | 是 | 確定是否使用為頂級資料夾設定的權限更新子級。 |
| 更新陣列 | `types:PermissionUpdateArray` | 是 | 要應用到資料夾的權限更新陣列。 |

**輸出(updateFolderPermissionsReturn)**

IPS API不會為此操作返迴響應。

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
