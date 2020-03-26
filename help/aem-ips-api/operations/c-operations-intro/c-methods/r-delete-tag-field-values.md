---
description: 從標籤欄位的字典中移除標籤欄位值。
seo-description: 從標籤欄位的字典中移除標籤欄位值。
seo-title: deleteTagFieldValues
solution: Experience Manager
title: deleteTagFieldValues
topic: Scene7 Image Production System API
uuid: 71cdec4e-c1d6-4518-87ed-5c47a5112b15
translation-type: tm+mt
source-git-commit: b5eaefb375fbd0d0786619fa6d84b4f6fc17a77f

---


# deleteTagFieldValues{#deletetagfieldvalues}

從標籤欄位的字典中移除標籤欄位值。

## 授權使用者類型 {#section-e6f97c875c2a4cf0a7bc22096b649497}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 參數 {#section-5db64a6ae238426395bc760b83587260}

**輸入(deleteTagFieldValuesParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | 是 | 包含標籤欄位之公司的控制代碼。 |
| ` *`fieldHandle`*` | `xsd:string` | 是 | 要修改的標籤欄位的句柄。 |
| ` *`valueArray`*` | `types:StringArray` | 是 | 要從欄位字典中刪除的標籤值陣列。 |

**輸出(deleteTagFieldValuesParam)**

IPS API不會傳回此作業的回應。

## 範例 {#section-92f9e575a6da491caa09e264b4d6ee55}

**請求**

```java
deleteTagFieldValuesParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <fieldHandle>m|3|ASSET|SingleFixedTag</fieldHandle>
   <valueArray>
      <items>Pineapple</items>
      <items>Banana</items>
   </valueArray>
</deleteTagFieldValuesParam>
```

**回答**

無。
