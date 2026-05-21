---
description: 更新檔案夾許可權。
solution: Experience Manager
title: updateFolderPermissions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 4e4f382e-4339-4b9d-a721-d33a4fa8be6b
TQID: 'https://experienceleague.adobe.com/rZv5saDJ9TTY7IYvE6i6CZIHX9xqx9HFnIJTQxdbjPU'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 73
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
