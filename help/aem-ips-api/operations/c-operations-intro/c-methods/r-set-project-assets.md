---
description: 指派或更新專案中的資產。
solution: Experience Manager
title: setprojectassets
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: b6e6e9bd-5ee2-4750-9182-49e7a3e3486c
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 18%

---

# setprojectassets{#setprojectassets}

指派或更新專案中的資產。

語法

## 授權的使用者型別 {#section-8d87939db6d547b48ca6d71771bbefa8}

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
| companyName | `xsd:string` | 是 | 公司控制代碼。 |
| projectHandle | `xsd:string` | 是 | 專案控制代碼。 |
| assetHandleArray | `types:HandleArray` | 是 | 您要與專案關聯的資產控制代碼陣列。 |

**輸出(setProjectAssetsReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| successCount | `xsd:int` | 是 | 成功新增的資產數目。 |

## 範例 {#section-33c1a909c3dc4aa98da474c23a036596}

此程式碼範例將資產指派給專案。 要求傳回成功計數1。

**要求**

```java
<setProjectAssetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <projectHandle>p|6|ProjectTestAPI</projectHandle>
   <assetHandleArray>
      <items>a|739|1|537</items>
   </assetHandleArray>
</setProjectAssetsParam>
```

**回應**

```java
<setProjectAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</setProjectAssetsReturn>
```
