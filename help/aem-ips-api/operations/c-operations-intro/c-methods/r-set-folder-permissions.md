---
description: 設定資料夾權限。
solution: Experience Manager
title: setFolderPermissions
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 0da05679-207e-4dc8-9bfe-2cf09a8c3f17
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 14%

---

# setFolderPermissions{#setfolderpermissions}

設定資料夾權限。

語法

## 授權的使用者類型 {#section-d3eb923fcf5741b99967634db809e09e}

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

IPS API不會針對此操作傳回回應。

## 範例 {#section-01730da4be874553ab44e3241cdf6357}

此程式碼範例會指定公司控制代碼、資料夾控制代碼，以及包含資料夾詳細資訊的權限陣列。 它會對父資料夾的子資料夾套用相同的權限。

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
