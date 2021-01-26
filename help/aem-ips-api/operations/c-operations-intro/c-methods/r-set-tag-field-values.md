---
description: 設定現有標籤欄位的標籤字典值。
seo-description: 設定現有標籤欄位的標籤字典值。
seo-title: setTagFieldValues
solution: Experience Manager
title: setTagFieldValues
topic: Dynamic Media Image Production System API
uuid: 56666c00-3694-4a43-a0ff-97af45c8df9f
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 15%

---


# setTagFieldValues{#settagfieldvalues}

設定現有標籤欄位的標籤字典值。

語法

## 授權用戶類型{#section-8b1413654bab44cfb2b1fffbb88aa385}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 參數 {#section-a05cbee4cb4f44198c414a6b14e69156}

**輸入**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 公司負責人。 |
| `*`fieldHandle`*` | `xsd:string` | 是 | 標籤欄位控制代碼。 |
| `*`valueArray`*` | `types:StringArray` | 是 | 一組標籤值，用於替換欄位的現有字典。 當新值與現有值相符時，會維護資產關聯。 |

**輸出(setTagFieldValuesReturn)**

IPS API不會傳回此作業的回應。

## 範例 {#section-b11cafd9bed54ab5836c737cc075c918}

**請求**

```java
<setTagFieldValuesParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <fieldHandle>m|3|ASSET|SingleFixedTag</fieldHandle>
   <valueArray>
      <items>Nurth</items>
      <items>Suth</items>
      <items>East</items>
      <items>West</items>
      <items>Pineapple</items>
      <items>Banana</items>
   </valueArray>
</setTagFieldValuesParam>
```

**回答**

無。
