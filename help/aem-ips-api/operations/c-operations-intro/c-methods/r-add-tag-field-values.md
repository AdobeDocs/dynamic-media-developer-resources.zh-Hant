---
description: 將新標籤值添加到現有標籤欄位的字典中。
solution: Experience Manager
title: addTagFieldValues
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 099263e4-8214-46eb-898e-7a28c4f25598
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 14%

---

# addTagFieldValues{#addtagfieldvalues}

將新標籤值添加到現有標籤欄位的字典中。

語法

## 授權用戶類型 {#section-ba1d7040661e48b7a6b035494e065c91}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 參數 {#section-abe8893038bb4ddfaccc11a8c75e6bd0}

**輸入(addTagFieldValuesParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 公司句柄 | `xsd:string` | 是 | 包含標籤欄位的公司句柄。 |
| 欄位句柄 | `xsd:string` | 是 | 要修改的標籤欄位的句柄。 |
| 值陣列 | `xsd:string` | 是 | 要添加到欄位現有詞典的標籤值陣列。 |

**輸出(addTagFieldValuesParam)**

IPS API不會為此操作返迴響應。

## 範例 {#section-c4049392f1c548f883b8b1f8f167bada}

**請求**

```java {.line-numbers}
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
