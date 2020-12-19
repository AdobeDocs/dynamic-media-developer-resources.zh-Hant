---
description: 新增一或多個資產至專案。
seo-description: 新增一或多個資產至專案。
seo-title: addProjectAssets
solution: Experience Manager
title: addProjectAssets
topic: Scene7 Image Production System API
uuid: 48abea17-058e-4469-bb16-0abee8ef5214
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 11%

---


# addProjectAssets{#addprojectassets}

新增一或多個資產至專案。

語法

## 授權用戶類型{#section-c67e7422921047f4ab4d4e9ba5a7aafe}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 參數 {#section-20d498e971b6466298e60c8a77fc32b2}

**輸入(addProjectAssetsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | 是 | 處理至與目前專案相關聯的公司。 |
| ` *`projectHandle`*` | `xsd:string` | 是 | 處理您要新增資產至的專案。 |
| ` *`projectHandleArray`*` | `xsd:HandleArray` | 是 | 您要新增至目前專案的資產陣列。 |

**輸出(addProjectAssetsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| ` *`successCount`*` | `xsd:int` | 是 | 已成功新增資產的數目。 |
| ` *`warningCount`*` | `xsd:int` | 是 | 操作嘗試將資產添加到項目時生成的警告數。 |
| ` *`errorCount`*` | `xsd:int` | 是 | 嘗試將資產新增至專案時產生的錯誤數。 |
| ` *`warningDetailHandle`*` | `xsd:AssetOperationFaultArray` | 否 | 當操作嘗試將資產添加到項目時，資產生成的警告陣列。 |
| ` *`companyHandle`*` | `xsd:AssetOperationFaultArray` | 否 | 當操作嘗試將資產添加到項目時，資產生成的錯誤陣列。 |

## 範例 {#section-bee5be2402f54cb9a3a02cc07def4135}

此範例會將資產控制代碼陣列中的單一資產（由其控制代碼引用）新增至請求中指定的專案。 當響應`successCount`返回`1`時，操作成功完成。

**請求**

```java
<addProjectAssetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <projectHandle>p|6|ProjectTestAPI</projectHandle>
   <assetHandleArray>
      <items>a|732|1|535</items>
   </assetHandleArray>
</addProjectAssetsParam>
```

**回答**

```java
<addProjectAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</addProjectAssetsReturn>
```

