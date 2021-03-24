---
description: 指派或更新專案中的資產。
solution: Experience Manager
title: setProjectAssets
feature: Dynamic Media經典，SDK/API，資產管理
role: 開發人員、管理員
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 18%

---


# setProjectAssets{#setprojectassets}

指派或更新專案中的資產。

語法

## 授權用戶類型{#section-8d87939db6d547b48ca6d71771bbefa8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 參數 {#section-bd51ef23deaf434ba2efb8cef2a8b4a5}

**輸入(setProjectAssetsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyName`*` | `xsd:string` | 是 | 公司負責人。 |
| `*`projectHandle`*` | `xsd:string` | 是 | 專案控制代碼。 |
| `*`assetHandleArray`*` | `types:HandleArray` | 是 | 您要與專案關聯的資產控制代碼陣列。 |

**輸出(setProjectAssetsReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | 是 | 已成功新增資產的數目。 |

## 範例 {#section-33c1a909c3dc4aa98da474c23a036596}

此程式碼範例會指派資產給專案。 請求會傳回成功計數1。

**請求**

```java
<setProjectAssetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <projectHandle>p|6|ProjectTestAPI</projectHandle>
   <assetHandleArray>
      <items>a|739|1|537</items>
   </assetHandleArray>
</setProjectAssetsParam>
```

**回答**

```java
<setProjectAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</setProjectAssetsReturn>
```

