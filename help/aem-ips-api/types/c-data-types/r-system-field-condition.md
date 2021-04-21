---
description: searchAssets操作的系統欄位搜尋條件。
solution: Experience Manager
title: SystemFieldCondition
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 5%

---


# SystemFieldCondition{#systemfieldcondition}

searchAssets操作的系統欄位搜尋條件。

對於一元比較，根據系統欄位類型，只傳遞一個值（`boolVal`、`longVal`、`doubleVal`或`dateVal`）。 對於搜索範圍，請傳遞`min<Type>`和`max<Type>`參數，並傳遞`Between`或`NotBetween`的`op`值。

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| `*`欄位`*` | `xsd:string` | 「資產搜尋系統」欄位選擇。 |
| `*`op`*` | `xsd:string` | 字串比較運算子的選擇。 |
| `*`值`*` | `xsd:string` | 要測試的值。 |
| `*`boolVal`*` | `xsd:boolean` | 布林值比較值。 |
| `*`longVal`*` | `xsd:long` | 長比較值。 |
| `*`minLong`*` | `xsd:long` | 遠程下界。 |
| `*`maxLong`*` | `xsd:long` | 長程上界。 |
| `*`doubleVal`*` | `xsd:double` | 雙重比較值。 |
| `*`minDouble`*` | `xsd:double` | 雙程下界。 |
| `*`maxDouble`*` | `xsd:double` | 雙程上界。 |
| `*`dateVal`*` | `xsd:dateTime` | 日期比較值。 |
| `*`minDate`*` | `xsd:dateTime` | 日期範圍小。 |
| `*`maxDate`*` | `xsd:dateTime` | 日期範圍上限。 |

## 範例 {#section-347d4aabfff44530adba03d1dc0b9968}

```
<systemFieldConditionArray>
   <items>
      <field>LastModified</field>
      <op>Between</op>
      <minDate>2007-08-01T00:00:00</minDate>
      <maxDate>2007-12-01T00:00:00</maxDate>
   </items>
</systemFieldConditionArray>
```

