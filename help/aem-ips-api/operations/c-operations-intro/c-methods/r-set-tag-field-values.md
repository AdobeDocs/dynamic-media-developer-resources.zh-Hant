---
description: 為現有標籤欄位設定標籤字典值。
solution: Experience Manager
title: setTagFieldValues
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 50f437d6-fec5-4961-884e-fdb75d201ab7
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 16%

---

# setTagFieldValues{#settagfieldvalues}

為現有標籤欄位設定標籤字典值。

語法

## 授權的使用者類型 {#section-8b1413654bab44cfb2b1fffbb88aa385}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 參數 {#section-a05cbee4cb4f44198c414a6b14e69156}

**輸入**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 公司負責人。 |
| `*`fieldHandle`*` | `xsd:string` | 是 | 標籤欄位句柄。 |
| `*`valueArray`*` | `types:StringArray` | 是 | 取代欄位現有字典的標籤值陣列。 當新值符合現有值時，會維護資產關聯。 |

**輸出(setTagFieldValuesReturn)**

IPS API不會針對此操作傳回回應。

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
