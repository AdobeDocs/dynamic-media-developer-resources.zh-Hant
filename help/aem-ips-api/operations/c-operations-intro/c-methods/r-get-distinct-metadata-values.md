---
description: 傳回中繼資料欄位的所有值。
seo-description: 傳回中繼資料欄位的所有值。
seo-title: getDistinctMetadataValues
solution: Experience Manager
title: getDistinctMetadataValues
topic: Scene7 Image Production System API
uuid: 47c1d3a3-9f33-4c36-828a-e858370997d1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getDistinctMetadataValues{#getdistinctmetadatavalues}

傳回中繼資料欄位的所有值。

語法

## 授權使用者類型 {#section-f0f44fdcb318490582dd04de8eaf745d}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 參數 {#section-600f36a32ff147cb83149943d37843e2}

**輸入(getDistinctMetadataValuesParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | 是 | 您要取得資料之公司的控制代碼。 |
| ` *`metadataKey`*` | `xsd:string` | 是 | 以點符號表示的中繼資料金鑰。 |

**輸出(getDistinctMetadataValuesReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| ` *`valueArray`*` | `types:ValueArray` | 是 | 請求的元資料欄位的值。 |

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

