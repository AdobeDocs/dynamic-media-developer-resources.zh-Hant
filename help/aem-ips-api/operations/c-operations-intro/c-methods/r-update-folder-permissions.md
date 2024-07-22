---
description: 更新檔案夾許可權。
solution: Experience Manager
title: updateFolderPermissions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 4e4f382e-4339-4b9d-a721-d33a4fa8be6b
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 16%

---

# updateFolderPermissions{#updatefolderpermissions}

更新檔案夾許可權。

語法

## 授權的使用者型別 {#section-e5c2217231bf4b3386e0ab3f2e9aca0b}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 參數 {#section-339e6e17c5504e1ea79fbdc05f618050}

**輸入(updateFolderPermissionsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 公司控制代碼。 |
| folderHandle | `xsd:string` | 是 | 資料夾控制代碼。 |
| updateChildren | `xsd:boolean` | 是 | 決定是否使用為最上層檔案夾設定的許可權更新子系。 |
| updatearray | `types:PermissionUpdateArray` | 是 | 您要套用至資料夾的許可權更新陣列。 |

**輸出(updateFolderPermissionsReturn)**

IPS API未傳回此作業的回應。

## 範例 {#section-c3fe4d4388674870a3856c35ef66b631}

**要求**

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

**回應**

無。
