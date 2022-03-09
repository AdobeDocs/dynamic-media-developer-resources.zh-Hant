---
description: 設定資料夾權限。
solution: Experience Manager
title: setFolderPermissions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0da05679-207e-4dc8-9bfe-2cf09a8c3f17
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 15%

---

# setFolderPermissions{#setfolderpermissions}

設定資料夾權限。

語法

## 授權用戶類型 {#section-d3eb923fcf5741b99967634db809e09e}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 參數 {#section-2a41135054954396b40f1228f2e63b42}

**輸入(setFolderPermissionsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 公司句柄 | `xsd:string` | 是 | 公司負責。 |
| folderHandle | `xsd:string` | 是 | 資料夾句柄。 |
| setChildren | `xsd:boolean` | 是 | 設定屬於該資料夾的子項的權限。 |
| 權限陣列 | `types:PermissionUpdateArray` | 是 | 權限陣列。 |

**輸出(setFolderPermissionsReturn)**

IPS API不會為此操作返迴響應。

## 範例 {#section-01730da4be874553ab44e3241cdf6357}

此代碼示例指定了公司句柄、資料夾句柄和包含資料夾詳細資訊的權限陣列。 它對父資料夾的子資料夾應用相同的權限。

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
