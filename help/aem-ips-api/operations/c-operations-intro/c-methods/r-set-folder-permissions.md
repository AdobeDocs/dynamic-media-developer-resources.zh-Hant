---
description: 設定資料夾權限。
solution: Experience Manager
title: setFolderPermissions
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 14%

---


# setFolderPermissions{#setfolderpermissions}

設定資料夾權限。

語法

## 授權用戶類型{#section-d3eb923fcf5741b99967634db809e09e}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 參數 {#section-2a41135054954396b40f1228f2e63b42}

**輸入(setFolderPermissionsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 公司負責人。 |
| `*`folderHandle`*` | `xsd:string` | 是 | 資料夾句柄。 |
| `*`setChildren`*` | `xsd:boolean` | 是 | 設定屬於資料夾的子項的權限。 |
| `*`permissionArray`*` | `types:PermissionUpdateArray` | 是 | 權限陣列。 |

**輸出(setFolderPermissionsReturn)**

IPS API不會傳回此作業的回應。

## 範例 {#section-01730da4be874553ab44e3241cdf6357}

此程式碼範例會指定公司控制代碼、資料夾控制代碼和權限陣列，其中包含資料夾的詳細資訊。 它對父資料夾的子資料夾應用相同的權限。

**請求**

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

**回答**

無。
