---
description: 取得與資產相關聯的使用者定義中繼資料欄位。
solution: Experience Manager
title: getMetadataFields
feature: Dynamic Media Classic,SDK/API，中繼資料
role: Developer,Administrator
exl-id: 4d01e2e7-9b68-4dfa-9fe8-08a22cb4bfd5
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 14%

---

# getMetadataFields{#getmetadatafields}

取得與資產相關聯的使用者定義中繼資料欄位。

語法

## 授權的使用者類型 {#section-e32e481a02674b729bfc5454a6c9ff65}

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
| `*`companyHandle`*` | `xsd:string` | 是 | 公司負責人。 |
| `*`assetType`*` | `xsd:string` | 是 | 要從中取得中繼資料的資產類型。 |

**輸出(getMetadataFieldsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`代碼片語`*` | `Code Phrase` |  |  |

## 範例 {#section-dbfde1483d614b5aac2b491cb32115d7}

此程式碼範例會傳回指定類型和公司的中繼資料資產。 回應包含欄位陣列中的中繼資料欄位陣列。 並非所有資產都有相同的中繼資料。 IPS使用者會定義資產的中繼資料欄位。

**請求**

```java
<ns1:getMetadataFieldsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetType>Pdf</ns1:assetType>
</ns1:getMetadataFieldsParam>
```

**回答**

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
