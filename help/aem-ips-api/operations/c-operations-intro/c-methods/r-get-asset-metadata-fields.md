---
description: 傳回依資產類型分組的所有中繼資料欄位。
solution: Experience Manager
title: getAssetMetadataFields
feature: Dynamic Media經典，SDK/API，元資料，資產管理
role: 開發人員、管理員
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 20%

---


# getAssetMetadataFields{#getassetmetadatafields}

傳回依資產類型分組的所有中繼資料欄位。

語法

## 授權用戶類型{#section-e19a9d21cc2b45469c233d4ae55ebfc2}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 參數 {#section-5dd58970d61d4d4a928e36ffceca6f5e}

**輸入(getAssetMetadataFieldsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 您要擷取其中繼資料的公司的控制代碼。 |

**輸出(getAssetMetadataFieldsReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`assetFieldArray`*` | `types:AssetMetadataFieldsArray` | 是 | 中繼資料欄位的陣列，依資產類型區分。 |

## 範例 {#section-d79ab85f29144635b0b61416e52f4f3f}

**請求**

```java
<getAssetMetadataFieldsParam xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <companyHandle>c|1</companyHandle>
</getAssetMetadataFieldsParam>
```

**回答**

>[!NOTE]
>
>因簡短性而截斷。

```java
<getAssetMetadataFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <assetFieldsArray>
      <items>
         <assetType>Asset</assetType>
     </items>
   </assetFieldsArray>
<getAssetMetadataFieldsReturn>
```

