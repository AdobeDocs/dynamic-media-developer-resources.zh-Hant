---
description: 指派或更新專案中的資產。
solution: Experience Manager
title: setProjectAssets
feature: Dynamic Media Classic,SDK/API，資產管理
role: Developer,Administrator
exl-id: b6e6e9bd-5ee2-4750-9182-49e7a3e3486c
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 18%

---

# setProjectAssets{#setprojectassets}

指派或更新專案中的資產。

語法

## 授權的使用者類型 {#section-8d87939db6d547b48ca6d71771bbefa8}

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
| `*`assetHandleArray`*` | `types:HandleArray` | 是 | 您要與專案相關聯的資產控點陣列。 |

**輸出(setProjectAssetsReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | 是 | 已成功新增資產的數量。 |

## 範例 {#section-33c1a909c3dc4aa98da474c23a036596}

此程式碼範例會將資產指派給專案。 請求會傳回成功計數1。

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
