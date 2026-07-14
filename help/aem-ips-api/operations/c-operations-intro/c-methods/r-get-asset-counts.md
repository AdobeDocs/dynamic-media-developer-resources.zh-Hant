---
description: 取得與特定公司相關聯的資產和資產數目。
solution: Experience Manager
title: getAssetCounts
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 21cb8023-d6fe-416a-b16f-636df8a37958
TQID: 'https://experienceleague.adobe.com/gvFs-dqQ8oR38MTKrEYaap31BH-MtSaRtGtJd5FO-MY'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 141
ht-degree: 9%

---

# getAssetCounts{#getassetcounts}

取得與特定公司相關聯的資產和資產數目。

傳回的`countArray`包含`assetTypes` （資料型別`xsd:string`）的陣列，每個都具有自己的計數欄位（資料型別`xsd:int`），允許陣列的每個元素呈現多個資產型別。語法

## 授權的使用者型別 {#section-6234754722184e828352f10eb18fbce9}

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
| companyHandle | `xsd:string` | 是 | 擁有您要計算之資產的公司的控制代碼。 |

**輸出(getAssetCountsReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| countArray | `types:AssetCountArray` | 否 | 一連串資產型別，每個都有自己的計數欄位，可呈現陣列中每個元素的多個資產型別。 |

## 範例 {#section-6052a503eb3843f6adb99e200fdba280}

這個程式碼範例使用公司的控制代碼做為傳送至IPS Web服務伺服器之`getAssetCountsParam`中的欄位，以取得資產計數。

**要求**

```java
<getAssetCountsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
</getAssetCountsParam>
```

**回應**

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

