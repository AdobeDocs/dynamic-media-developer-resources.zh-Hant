---
description: 取得與特定公司相關的資產和資產數目。
seo-description: 取得與特定公司相關的資產和資產數目。
seo-title: getAssetCounts
solution: Experience Manager
title: getAssetCounts
topic: Dynamic Media Image Production System API
uuid: 92103806-59da-444f-b69c-d045d0ebf42e
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 9%

---


# getAssetCounts{#getassetcounts}

取得與特定公司相關的資產和資產數目。

傳回的`countArray`由`assetTypes`（資料類型`xsd:string`）的陣列組成，每個陣列都有自己的計數欄位（資料類型`xsd:int`），允許每個陣列元素呈現多種資產類型。
語法

## 授權用戶類型{#section-6234754722184e828352f10eb18fbce9}

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
| `*`companyHandle`*` | `xsd:string` | 是 | 您要計算資產的公司控制代碼。 |

**輸出(getAssetCountsReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`countArray`*` | `types:AssetCountArray` | 否 | 資產類型的陣列，每個資產類型都有自己的計數欄位，可讓每個陣列元素呈現多種資產類型。 |

## 範例 {#section-6052a503eb3843f6adb99e200fdba280}

此程式碼範例會將公司的控制代碼當做傳送至IPS網站伺服器的`getAssetCountsParam`欄位，以取得資產計數。

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

