---
description: 傳回中繼資料欄位的所有值。
solution: Experience Manager
title: getDistinctMetadataValues
feature: Dynamic Media Classic,SDK/API，中繼資料
role: Developer,Administrator
exl-id: 1987d8b0-64e4-49be-af45-98e4c6542e5f
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 22%

---

# getDistinctMetadataValues{#getdistinctmetadatavalues}

傳回中繼資料欄位的所有值。

語法

## 授權的使用者類型 {#section-f0f44fdcb318490582dd04de8eaf745d}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 參數 {#section-600f36a32ff147cb83149943d37843e2}

**Input(getDistinctMetadataValuesParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 您要取得資料之公司的控制代碼。 |
| `*`metadataKey`*` | `xsd:string` | 是 | 以點記號表示的中繼資料索引鍵。 |

**Output(getDistinctMetadataValuesReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`valueArray`*` | `types:ValueArray` | 是 | 請求的元資料欄位的值。 |

## 範例 {#section-0189fa6fb31646cda5ce1b0bc4fcdf46}

**請求**

```java
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/"
xmlns:xsd="http://www.scene7.com/IpsApi/xsd"
xmlns:ns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <soapenv:Header>
      <xsd:authHeader>
         <xsd:user>user@company.com</xsd:user>
         <xsd:password>password</xsd:password>
      </xsd:authHeader>
   </soapenv:Header>
   <soapenv:Body>
   <ns:getDistinctMetadataValuesParam>
      <ns:companyHandle>680</ns:companyHandle>
      <ns:metadataKey>dc.format</ns:metadataKey>
      </ns:getDistinctMetadataValuesParam>
   </soapenv:Body>
</soapenv:Envelope>
```

**回答**

```java
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/">
   <soapenv:Body>
      <getDistinctMetadataValuesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
         <valueArray>
            <items>
               <value>N/A</value>
               <count>412</count>
            </items>
            <items>
               <value>image/jpeg</value>
               <count>189</count>
            </items>
            <items>
               <value>image/epsf</value>
               <count>1</count>
            </items>
            <items>
               <value>image/tiff</value>
               <count>3</count>
            </items>
         </valueArray>
      </getDistinctMetadataValuesReturn>
   </soapenv:Body>
</soapenv:Envelope>
```
