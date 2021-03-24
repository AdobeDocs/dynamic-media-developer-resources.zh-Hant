---
description: 更新資產集。
solution: Experience Manager
title: updateAssetSet
feature: Dynamic Media經典，SDK/API，資產管理
role: 開發人員、管理員
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 19%

---


# updateAssetSet{#updateassetset}

更新資產集。

語法

## 參數 {#section-d7080ccd97334c94860eb107a3e132b2}

**輸入(updateAssetSetParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 包含您要修改之影像集之公司的控制代碼。 |
| `*`assetHandle`*` | `xsd:string` | 是 | 要修改的影像集的控點。 |
| `*`setDefinition`*` | `xsd:string` | 否 | 重設影像整合員。 |
| `*`thumbAssetHandle`*` | `xsd:string` | 否 | 當做影像集縮圖的資產控點。 |

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

