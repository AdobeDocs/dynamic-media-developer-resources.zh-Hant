---
description: 傳回依資產類型分組的所有中繼資料欄位。
solution: Experience Manager
title: getAssetMetadataFields
feature: Dynamic Media Classic, SDK/API，中繼資料，資產管理
role: Developer,Administrator
exl-id: 5234d3ea-c333-4e35-91ae-ce3412919fda
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 21%

---

# getAssetMetadataFields{#getassetmetadatafields}

傳回依資產類型分組的所有中繼資料欄位。

語法

## 授權的使用者類型 {#section-e19a9d21cc2b45469c233d4ae55ebfc2}

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
| `*`assetFieldArray`*` | `types:AssetMetadataFieldsArray` | 是 | 中繼資料欄位陣列，依資產類型。 |

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
>為簡潔而截斷。

```java
<getAssetMetadataFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <assetFieldsArray>
      <items>
         <assetType>Asset</assetType>
     </items>
   </assetFieldsArray>
<getAssetMetadataFieldsReturn>
```
