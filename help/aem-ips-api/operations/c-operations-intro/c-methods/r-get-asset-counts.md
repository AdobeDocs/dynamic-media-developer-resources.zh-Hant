---
description: 取得與特定公司相關聯的資產和資產數量。
solution: Experience Manager
title: getAssetCounts
feature: Dynamic Media Classic,SDK/API，資產管理
role: Developer,Administrator
exl-id: 21cb8023-d6fe-416a-b16f-636df8a37958
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 10%

---

# getAssetCounts{#getassetcounts}

取得與特定公司相關聯的資產和資產數量。

傳回的`countArray`由`assetTypes`（資料類型`xsd:string`）陣列組成，每個陣列都有其自己的計數欄位（資料類型`xsd:int`），可讓每個陣列元素呈現多個資產類型。
語法

## 授權的使用者類型 {#section-6234754722184e828352f10eb18fbce9}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 參數 {#section-2a9581315eca427d8a3d26cc3fca7b1f}

**輸入(getAssetCountsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 含有您要計算之資產之公司的控制代碼。 |

**輸出(getAssetCountsReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`countArray`*` | `types:AssetCountArray` | 否 | 資產類型的陣列，每個都具有自己的計數欄位，可讓陣列的每個元素呈現多個資產類型。 |

## 範例 {#section-6052a503eb3843f6adb99e200fdba280}

此代碼示例將公司的句柄用作發送到IPS Web服務伺服器的`getAssetCountsParam`中的欄位，以獲取資產計數。

**請求**

```java
<getAssetCountsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
</getAssetCountsParam>
```

**回答**

```java
<getAssetCountsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <countArray>
      <items>
         <assetType>Image</assetType>
         <count>44</count>
      </items>
      <items>
         <assetType>Flash</assetType>
         <count>3</count>
      </items>
   </countArray>
</getAssetCountsReturn>
```
