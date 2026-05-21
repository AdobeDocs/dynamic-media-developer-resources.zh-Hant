---
description: 設定資產的中繼資料值。 使用一系列中繼資料更新，以設定批次中的值。
solution: Experience Manager
title: setAssetMetadata
feature: Dynamic Media Classic,SDK/API,Metadata,Asset Management
role: Developer,Admin
exl-id: 811e44e1-774a-49bd-a2bd-a7504e5f7f5f
TQID: 'https://experienceleague.adobe.com/b8E8BK8pyJQiYlR2yNMbYPWcLVNfmAvI5WaOBuaBz1E'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 123
ht-degree: 8%

---

# setAssetMetadata{#setassetmetadata}

設定資產的中繼資料值。 使用一系列中繼資料更新，以設定批次中的值。

語法

## 授權的使用者型別 {#section-9dcacb0c924044648f8324bfed183dca}

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
| companyHandle | `xsd:string` | 是 | 擁有您要更新之資產的公司的控制代碼。 |
| assetHandle | `xsd:string` | 是 | 資產的控點。 |
| updatearray | `types:MetadataUpdateArray` | 是 | 中繼資料更新陣列中的更新。 |

**輸出(setAssetMetadataReturn)**

IPS API未傳回此作業的回應。

## 範例 {#section-1ab412e7ee1d4d6d8469b0b403598c42}

此程式碼範例使用一系列中繼資料更新來設定指定資產的中繼資料。

**要求**

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

**回應**

無。
