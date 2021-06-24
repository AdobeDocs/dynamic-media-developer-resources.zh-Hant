---
description: 新增一或多個資產至專案。
solution: Experience Manager
title: addProjectAssets
feature: Dynamic Media Classic,SDK/API，資產管理
role: Developer,Administrator
exl-id: 60aa2846-b41e-4131-b465-82aa832434f7
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 11%

---

# addProjectAssets{#addprojectassets}

新增一或多個資產至專案。

語法

## 授權的使用者類型 {#section-c67e7422921047f4ab4d4e9ba5a7aafe}

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
| `*`companyHandle`*` | `xsd:string` | 是 | 處理與當前項目關聯的公司。 |
| `*`projectHandle`*` | `xsd:string` | 是 | 處理您要新增資產的專案。 |
| `*`projectHandleArray`*` | `xsd:HandleArray` | 是 | 您要新增至目前專案的資產陣列。 |

**輸出(addProjectAssetsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | 是 | 已成功新增資產的數量。 |
| `*`warningCount`*` | `xsd:int` | 是 | 操作嘗試將資產添加到項目時生成的警告數。 |
| `*`errorCount`*` | `xsd:int` | 是 | 操作嘗試將資產添加到項目時生成的錯誤數。 |
| `*`warningDetailHandle`*` | `xsd:AssetOperationFaultArray` | 否 | 資產嘗試將其新增至專案時產生的警告陣列。 |
| `*`companyHandle`*` | `xsd:AssetOperationFaultArray` | 否 | 資產嘗試將其新增至專案時產生的錯誤陣列。 |

## 範例 {#section-bee5be2402f54cb9a3a02cc07def4135}

此範例會將資產控制代碼陣列中的單一資產（由其控制代碼參考）新增至請求中指定的專案。 當響應`successCount`返回`1`時，操作已成功完成。

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
