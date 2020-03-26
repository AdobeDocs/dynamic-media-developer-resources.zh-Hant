---
description: 新增標籤值至現有標籤欄位的字典。
seo-description: 新增標籤值至現有標籤欄位的字典。
seo-title: addTagFieldValues
solution: Experience Manager
title: addTagFieldValues
topic: Scene7 Image Production System API
uuid: 9304f02c-a1df-4477-ab33-f2491c390c92
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# addTagFieldValues{#addtagfieldvalues}

新增標籤值至現有標籤欄位的字典。

語法

## 授權使用者類型 {#section-ba1d7040661e48b7a6b035494e065c91}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 參數 {#section-abe8893038bb4ddfaccc11a8c75e6bd0}

**輸入(addTagFieldValuesParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | 是 | 包含標籤欄位之公司的控制代碼。 |
| ` *`fieldHandle`*` | `xsd:string` | 是 | 要修改的標籤欄位的句柄。 |
| ` *`valueArray`*` | `xsd:string` | 是 | 要新增至欄位現有字典的標籤值陣列。 |

**輸出(addTagFieldValuesParam)**

IPS API不會傳回此作業的回應。

## 範例 {#section-c4049392f1c548f883b8b1f8f167bada}

**請求**

```java
<addTagFieldValuesParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <fieldHandle>m|3|ASSET|SingleFixedTag</fieldHandle>
   <valueArray>
      <items>Pineapple</items>
      <items>Banana</items>
   </valueArray>
</addTagFieldValuesParam>
```

**回答**

無。
