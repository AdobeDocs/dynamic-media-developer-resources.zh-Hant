---
description: 設定檔案夾許可權。
solution: Experience Manager
title: setFolderPermissions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0da05679-207e-4dc8-9bfe-2cf09a8c3f17
TQID: 'https://experienceleague.adobe.com/r-WGRjE263vPSVKsBieklQ79SASbDQOx9hp5IzS0-O0'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 6762cee83f1b7c970ed6353450c2ae6c602e7f3a
workflow-type: tm+mt
source-wordcount: 91
ht-degree: 13%

---

# setFolderPermissions{#setfolderpermissions}

設定檔案夾許可權。

語法

## 授權的使用者型別 {#section-d3eb923fcf5741b99967634db809e09e}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 參數 {#section-2a41135054954396b40f1228f2e63b42}

**輸入(setFolderPermissionsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 公司控制代碼。 |
| folderHandle | `xsd:string` | 是 | 資料夾控制代碼。 |
| setchildren | `xsd:boolean` | 是 | 設定屬於資料夾之子項的許可權。 |
| permissionArray | `types:PermissionUpdateArray` | 是 | 許可權陣列。 |

**輸出(setFolderPermissionsReturn)**

IPS API未傳回此作業的回應。

## 範例 {#section-01730da4be874553ab44e3241cdf6357}

此程式碼範例指定公司控制代碼、資料夾控制代碼和許可權陣列，其中包含有關資料夾的詳細資訊。 它會套用父資料夾子項的相同許可權。

**要求**

```java
<setFolderPermissionsParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>64</companyHandle>
   <folderHandle>blackmesa/Awatermark/</folderHandle>
   <setChildren>true</setChildren>
   <permissionArray>
      <items>
         <groupHandle>521</groupHandle>
         <permissionType>Read</permissionType>
         <isAllowed>true</isAllowed>
         <isOverride>true</isOverride>
      </items>
   </permissionArray>
</setFolderPermissionsParam>
```

**回應**

無。

