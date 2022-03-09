---
description: 從項目中刪除資產。 不會毀掉資產。
solution: Experience Manager
title: 刪除ProjectAssets
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 6bf169ec-c724-4ac0-a2bf-67af2ebba21a
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 11%

---

# 刪除ProjectAssets{#removeprojectassets}

從項目中刪除資產。 不會毀掉資產。

語法

## 授權用戶類型 {#section-b0b333a1f3b648ac8cd6bb3d135d2c6f}

* `IpsUser`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 參數 {#section-169d8e317417415b87df86242f65710e}

**輸入(removeProjectAssetsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 公司句柄 | `xsd:string` | 是 | 要移動的資產的公司的句柄。 |
| 項目句柄 | `xsd:string` | 是 | 要移動的項目資產的句柄。 |
| assetHandleArray | `types:HandleArray` | 是 | 要移動的資產的句柄陣列。 |

**輸出(removeProjectAssetsReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 成功計數 | `xsd:int` | 是 | 已成功刪除資產計數。 |
| 警告計數 | `xsd:int` | 是 | 操作嘗試從項目中刪除資產時生成的警告數。 |
| 錯誤計數 | `xsd:int` | 是 | 操作嘗試從項目中刪除資產時生成的錯誤數。 |
| 警告DetailArray | `types:AssetOperationFaultArray` | 否 | 與在操作嘗試從項目中刪除時生成警告的資產關聯的詳細資訊陣列。 |
| 錯誤DetailArray | `types:AssetOperationFaultArray` | 否 | 與在操作嘗試從項目中刪除錯誤時生成錯誤的資產關聯的詳細資訊陣列。 |

## 範例 {#section-13546cf0a98e4e1b91b8b7cd5724ced8}

此代碼示例從項目中刪除2個資產（由項目句柄指定）。

**請求**

```java
<removeProjectAssetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <projectHandle>p|6|ProjectTestAPI</projectHandle>
   <assetHandleArray>
      <items>a|732|1|535</items>
      <items>a|739|1|537</items>
   </assetHandleArray>
</removeProjectAssetsParam>
```
