---
description: 更新資產集。
solution: Experience Manager
title: 更新資產集
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: af7899c4-a95f-42c8-858e-ed1592c6f5b6
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 22%

---

# 更新資產集{#updateassetset}

更新資產集。

語法

## 參數 {#section-d7080ccd97334c94860eb107a3e132b2}

**輸入(updateAssetSetParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 公司句柄 | `xsd:string` | 是 | 包含要修改的映像集的公司的句柄。 |
| 資產句柄 | `xsd:string` | 是 | 要修改的影像集的句柄。 |
| setDefinition | `xsd:string` | 否 | 重置影像整合員。 |
| 拇指資產句柄 | `xsd:string` | 否 | 用作影像集縮略圖的資產句柄。 |

**輸出(updateAssetSetReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
|  |  |  |  |

## 範例 {#section-ce47a4b6e062423fa55ed3a0fd26d7ff}

**請求**

```java
<updateAssetSetParam xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"> 
  <companyHandle>c|15</companyHandle> 
  <assetHandle>a|535</assetHandle> 
  <setDefinition>${getCatalogId([a|202])};${getCatalogId([a|202])};advanced_image;,${getCatalogId([a|935])};${getCatalogId([a|935])};advanced_image;,${getCatalogId([a|933])};${getCatalogId([a|933])};advanced_image;</setDefinition> 
  <thumbAssetHandle>a|202</thumbAssetHandle> 
</updateAssetSetParam>
```

**回答**

```java
<updateAssetSetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"/>
```
