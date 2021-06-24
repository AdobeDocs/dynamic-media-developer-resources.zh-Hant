---
description: 從專案移除資產。 不會銷毀資產。
solution: Experience Manager
title: removeProjectAssets
feature: Dynamic Media Classic,SDK/API，資產管理
role: Developer,Administrator
exl-id: 6bf169ec-c724-4ac0-a2bf-67af2ebba21a
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 10%

---

# removeProjectAssets{#removeprojectassets}

從專案移除資產。 不會銷毀資產。

語法

## 授權的使用者類型 {#section-b0b333a1f3b648ac8cd6bb3d135d2c6f}

* `IpsUser`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 參數 {#section-169d8e317417415b87df86242f65710e}

**輸入(removeProjectAssetsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 含有您要移動資產的公司控制代碼。 |
| `*`projectHandle`*` | `xsd:string` | 是 | 您要移動之專案資產的控制代碼。 |
| `*`assetHandleArray`*` | `types:HandleArray` | 是 | 要移動的資產的控點陣列。 |

**輸出(removeProjectAssetsReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | 是 | 已成功移除資產計數。 |
| `*`warningCount`*` | `xsd:int` | 是 | 操作嘗試從項目中刪除資產時生成的警告數。 |
| `*`errorCount`*` | `xsd:int` | 是 | 嘗試從專案移除資產時產生的錯誤數。 |
| `*`warningDetailArray`*` | `types:AssetOperationFaultArray` | 否 | 與資產相關聯的詳細資訊陣列，當操作嘗試從專案中移除資產時，資產會產生警告。 |
| `*`errorDetailArray`*` | `types:AssetOperationFaultArray` | 否 | 與操作嘗試從專案移除時產生錯誤之資產相關聯的詳細資訊陣列。 |

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
