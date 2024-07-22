---
description: 傳回所有中繼資料欄位，依資產型別分組。
solution: Experience Manager
title: getassetmetadataFields
feature: Dynamic Media Classic,SDK/API,Metadata,Asset Management
role: Developer,Admin
exl-id: 5234d3ea-c333-4e35-91ae-ce3412919fda
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 20%

---

# getassetmetadataFields{#getassetmetadatafields}

傳回所有中繼資料欄位，依資產型別分組。

語法

## 授權的使用者型別 {#section-e19a9d21cc2b45469c233d4ae55ebfc2}

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
| companyHandle | `xsd:string` | 是 | 您要擷取其中繼資料之公司的控制代碼。 |

**輸出(getAssetMetadataFieldsReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| assetFieldArray | `types:AssetMetadataFieldsArray` | 是 | 中繼資料欄位陣列（依資產型別）。 |

## 範例 {#section-d79ab85f29144635b0b61416e52f4f3f}

**要求**

```java
<getAssetMetadataFieldsParam xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <companyHandle>c|1</companyHandle>
</getAssetMetadataFieldsParam>
```

**回應**

>[!NOTE]
>
>為簡短起見，已截斷。

```java
<getAssetMetadataFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <assetFieldsArray>
      <items>
         <assetType>Asset</assetType>
     </items>
   </assetFieldsArray>
<getAssetMetadataFieldsReturn>
```
