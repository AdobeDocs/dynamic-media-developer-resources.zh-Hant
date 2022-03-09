---
description: 獲取與特定公司關聯的資產和資產數。
solution: Experience Manager
title: getAssetCounts
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 21cb8023-d6fe-416a-b16f-636df8a37958
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 10%

---

# getAssetCounts{#getassetcounts}

獲取與特定公司關聯的資產和資產數。

的 `countArray` 返回的 `assetTypes` （資料類型） `xsd:string`)，每個都有自己的計數欄位（資料類型） `xsd:int`)，允許表示每個陣列元素的多個資產類型。
語法

## 授權用戶類型 {#section-6234754722184e828352f10eb18fbce9}

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
| 公司句柄 | `xsd:string` | 是 | 要計算資產的公司的句柄。 |

**輸出(getAssetCountsReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 計數陣列 | `types:AssetCountArray` | 否 | 資產類型的陣列，每個資產類型都有其自己的計數欄位，允許對每個陣列元素表示多個資產類型。 |

## 範例 {#section-6052a503eb3843f6adb99e200fdba280}

此代碼示例將公司的句柄用作 `getAssetCountsParam` 發送到IPS Web服務伺服器以獲取資產計數。

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
