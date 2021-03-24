---
description: 從專案移除資產。 不銷毀資產。
solution: Experience Manager
title: removeProjectAssets
feature: Dynamic Media經典，SDK/API，資產管理
role: 開發人員、管理員
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 10%

---


# removeProjectAssets{#removeprojectassets}

從專案移除資產。 不銷毀資產。

語法

## 授權用戶類型{#section-b0b333a1f3b648ac8cd6bb3d135d2c6f}

* `IpsUser`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 參數 {#section-169d8e317417415b87df86242f65710e}

**輸入(removeProjectAssetsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 您要移動資產的公司控制代碼。 |
| `*`projectHandle`*` | `xsd:string` | 是 | 您要移動的專案資產的控制代碼。 |
| `*`assetHandleArray`*` | `types:HandleArray` | 是 | 要移動的資產的控制代碼陣列。 |

**輸出(removeProjectAssetsReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | 是 | 已成功移除資產計數。 |
| `*`warningCount`*` | `xsd:int` | 是 | 操作嘗試從項目中刪除資產時生成的警告數。 |
| `*`errorCount`*` | `xsd:int` | 是 | 嘗試從專案移除資產時產生的錯誤數。 |
| `*`warningDetailArray`*` | `types:AssetOperationFaultArray` | 否 | 與資產相關的詳細資訊陣列，當操作嘗試從專案中移除資產時，這些資產會產生警告。 |
| `*`errorDetailArray`*` | `types:AssetOperationFaultArray` | 否 | 當操作嘗試從項目中刪除錯誤時，與產生錯誤的資產相關的詳細資訊陣列。 |

## 範例 {#section-13546cf0a98e4e1b91b8b7cd5724ced8}

此程式碼範例會從專案中移除2個資產（由專案控制代碼指定）。

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

