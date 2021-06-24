---
description: 設定資產的中繼資料值。 搭配中繼資料更新的陣列使用，以在批次中設定值。
solution: Experience Manager
title: setAssetMetadata
feature: Dynamic Media Classic, SDK/API，中繼資料，資產管理
role: Developer,Administrator
exl-id: 811e44e1-774a-49bd-a2bd-a7504e5f7f5f
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 9%

---

# setAssetMetadata{#setassetmetadata}

設定資產的中繼資料值。 搭配中繼資料更新的陣列使用，以在批次中設定值。

語法

## 授權的使用者類型 {#section-9dcacb0c924044648f8324bfed183dca}

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
| `*`companyHandle`*` | `xsd:string` | 是 | 含有您要更新之資產之公司的控制代碼。 |
| `*`assetHandle`*` | `xsd:string` | 是 | 資產的控制代碼。 |
| `*`updateArray`*` | `types:MetadataUpdateArray` | 是 | 中繼資料更新陣列中的更新。 |

**輸出(setAssetMetadataReturn)**

IPS API不會針對此操作傳回回應。

## 範例 {#section-1ab412e7ee1d4d6d8469b0b403598c42}

此程式碼範例使用中繼資料更新的陣列，來設定指定資產的中繼資料。

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
