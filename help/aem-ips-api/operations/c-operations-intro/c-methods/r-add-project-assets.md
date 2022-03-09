---
description: 向項目添加一個或多個資產。
solution: Experience Manager
title: addProjectAssets
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 60aa2846-b41e-4131-b465-82aa832434f7
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 11%

---

# addProjectAssets{#addprojectassets}

向項目添加一個或多個資產。

語法

## 授權用戶類型 {#section-c67e7422921047f4ab4d4e9ba5a7aafe}

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
| 公司句柄 | `xsd:string` | 是 | 處理與當前項目關聯的公司。 |
| 項目句柄 | `xsd:string` | 是 | 處理要向其添加資產的項目。 |
| projectHandleArray | `xsd:HandleArray` | 是 | 要添加到當前項目的資產陣列。 |

**輸出(addProjectAssetsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 成功計數 | `xsd:int` | 是 | 已成功添加的資產數。 |
| 警告計數 | `xsd:int` | 是 | 操作嘗試將資產添加到項目時生成的警告數。 |
| 錯誤計數 | `xsd:int` | 是 | 操作嘗試將資產添加到項目時生成的錯誤數。 |
| 警告DetailHandle | `xsd:AssetOperationFaultArray` | 否 | 當操作嘗試將資產添加到項目時由資產生成的警告陣列。 |
| 公司句柄 | `xsd:AssetOperationFaultArray` | 否 | 當操作嘗試將資產添加到項目時由資產生成的錯誤陣列。 |

## 範例 {#section-bee5be2402f54cb9a3a02cc07def4135}

此示例將資產句柄陣列中的單個資產（由其句柄引用）添加到請求中指定的項目。 響應時，操作成功完成 `successCount` 返回 `1`。

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
