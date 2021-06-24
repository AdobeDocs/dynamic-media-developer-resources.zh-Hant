---
description: 更新資產集。
solution: Experience Manager
title: updateAssetSet
feature: Dynamic Media Classic,SDK/API，資產管理
role: Developer,Administrator
exl-id: af7899c4-a95f-42c8-858e-ed1592c6f5b6
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 20%

---

# updateAssetSet{#updateassetset}

更新資產集。

語法

## 參數 {#section-d7080ccd97334c94860eb107a3e132b2}

**輸入(updateAssetSetParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 包含要修改的影像集的公司的句柄。 |
| `*`assetHandle`*` | `xsd:string` | 是 | 要修改的影像集的控點。 |
| `*`setDefinition`*` | `xsd:string` | 否 | 重置映像整合員。 |
| `*`thumbAssetHandle`*` | `xsd:string` | 否 | 作為影像集縮圖的資產控點。 |

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
