---
description: 取得唯一的中繼資料欄位值。
seo-description: 取得唯一的中繼資料欄位值。
seo-title: getUniqueMetadataValues
solution: Experience Manager
title: getUniqueMetadataValues
topic: Scene7 Image Production System API
uuid: 5b2f95a7-cc0b-4938-99b9-2aefa0ffe693
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 25%

---


# getUniqueMetadataValues{#getuniquemetadatavalues}

取得唯一的中繼資料欄位值。

語法

## 授權用戶類型{#section-6a6b67e10a4c4e7bb18306115713380e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 參數 {#section-b9d1413811c24566b6d095701f0f66db}

**輸入(getUniqueMetadataValuesParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | 是 | 為公司負責。 |
| ` *`fieldHandle`*` | `xsd:string` | 否 | 處理中繼資料欄位。 |

**輸出(getUniqueMetadataValuesReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| ` *`values`*` | `type:StringArray` |  |  |

## 範例 {#section-440f3bc3e5be436cb6ec26117d05f476}

此程式碼範例使用欄位控制代碼來傳回特定中繼資料值。

**請求**

```java
<ns1:getUniqueMetadataValuesParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:fieldHandle>47|ALL|Resolution</ns1:fieldHandle>
</ns1:getUniqueMetadataValuesParam>
```

**回答**

```java
<getUniqueMetadataValuesReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <values>
      <items>320</items>
   </values>
</getUniqueMetadataValuesReturn>
```

