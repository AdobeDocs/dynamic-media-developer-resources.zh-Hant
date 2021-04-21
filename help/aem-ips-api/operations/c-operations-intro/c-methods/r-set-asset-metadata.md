---
description: 設定資產的中繼資料值。 可搭配一組中繼資料更新，以設定批次中的值。
solution: Experience Manager
title: setAssetMetadata
feature: Dynamic Media Classic,SDK/API,Metadata,Asset Management
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 9%

---


# setAssetMetadata{#setassetmetadata}

設定資產的中繼資料值。 可搭配一組中繼資料更新，以設定批次中的值。

語法

## 授權用戶類型{#section-9dcacb0c924044648f8324bfed183dca}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>使用者必須擁有資產的讀取存取權。

## 參數 {#section-bcdcff30905e444388811e897b2824bd}

**輸入(setAssetMetadataParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 包含您要更新資產之公司的控制代碼。 |
| `*`assetHandle`*` | `xsd:string` | 是 | 資產的控制代碼。 |
| `*`updateArray`*` | `types:MetadataUpdateArray` | 是 | 中繼資料更新陣列中的更新。 |

**輸出(setAssetMetadataReturn)**

IPS API不會傳回此作業的回應。

## 範例 {#section-1ab412e7ee1d4d6d8469b0b403598c42}

此程式碼範例使用中繼資料更新陣列來設定指定資產的中繼資料。

**請求**

```java
<ns1:setAssetMetadataParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>24265|1|17061</ns1:assetHandle>
   <ns1:updateArray>
      <ns1:items>
         <ns1:fieldHandle>47|ALL|Resolution</ns1:fieldHandle>
         <ns1:value>320</ns1:value>
      </ns1:items>
   </ns1:updateArray>
</ns1:setAssetMetadataParam>
```

**回答**

無。
