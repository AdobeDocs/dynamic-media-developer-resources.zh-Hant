---
description: 返回按資產類型分組的所有元資料欄位。
solution: Experience Manager
title: getAssetMetadataFields
feature: Dynamic Media Classic,SDK/API,Metadata,Asset Management
role: Developer,Admin
exl-id: 5234d3ea-c333-4e35-91ae-ce3412919fda
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 23%

---

# getAssetMetadataFields{#getassetmetadatafields}

返回按資產類型分組的所有元資料欄位。

語法

## 授權用戶類型 {#section-e19a9d21cc2b45469c233d4ae55ebfc2}

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
| 公司句柄 | `xsd:string` | 是 | 要檢索其元資料的公司的句柄。 |

**輸出(getAssetMetadataFieldsReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| assetFieldArray | `types:AssetMetadataFieldsArray` | 是 | 按資產類型列出的元資料欄位陣列。 |

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
>為簡單而截斷。

```java
<getAssetMetadataFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <assetFieldsArray>
      <items>
         <assetType>Asset</assetType>
     </items>
   </assetFieldsArray>
<getAssetMetadataFieldsReturn>
```
