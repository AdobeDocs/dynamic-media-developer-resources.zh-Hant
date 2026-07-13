---
description: 取得與資產相關聯的使用者定義中繼資料欄位。
solution: Experience Manager
title: getMetadataFields
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: 4d01e2e7-9b68-4dfa-9fe8-08a22cb4bfd5
TQID: 'https://experienceleague.adobe.com/MA5Y2w4x49b36L6s4PICphm1iamWmVdj-BSMmOQxMdA'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 97
ht-degree: 13%

---

# getMetadataFields{#getmetadatafields}

取得與資產相關聯的使用者定義中繼資料欄位。

語法

## 授權的使用者型別 {#section-e32e481a02674b729bfc5454a6c9ff65}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 參數 {#section-bac949e59c0546429c5786fe422d750d}

**輸入(getMetadataFieldsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 公司控制代碼。 |
| assetType | `xsd:string` | 是 | 從中取得中繼資料的資產型別。 |

**輸出(getMetadataFieldsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 程式碼片語 | `Code Phrase` |  |  |

## 範例 {#section-dbfde1483d614b5aac2b491cb32115d7}

此程式碼範例會傳回指定型別和公司的中繼資料資產。 回應包含欄位陣列中的中繼資料欄位陣列。 並非所有資產都具有相同的中繼資料。 ips使用者會定義資產的中繼資料欄位。

**要求**

```java
<ns1:getMetadataFieldsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetType>Pdf</ns1:assetType>
</ns1:getMetadataFieldsParam>
```

**回應**

```java
<getMetadataFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <fieldArray>
      <items>
         <fieldHandle>47|ALL|Resolution</fieldHandle>
         <name>Resolution</name>
         <type>String</type>
         <defaultValue>120</defaultValue>
         <isRequired>false</isRequired>
         <isUserDefined>true</isUserDefined>
      </items>
   </fieldArray>
</getMetadataFieldsReturn>
```

