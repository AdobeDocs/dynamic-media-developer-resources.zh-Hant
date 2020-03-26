---
description: searchAssets操作的系統欄位搜尋條件。
seo-description: searchAssets操作的系統欄位搜尋條件。
seo-title: SystemFieldCondition
solution: Experience Manager
title: SystemFieldCondition
topic: Scene7 Image Production System API
uuid: 811095df-732d-48a3-a6ff-55d6dc602b54
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SystemFieldCondition{#systemfieldcondition}

searchAssets操作的系統欄位搜尋條件。

對於一元比較，根據系統欄位 `boolVal`類型 `longVal`，只 `doubleVal`要傳遞一個值( `dateVal`、或)。 對於搜尋範圍，請 `min<Type>` 傳遞 `max<Type>` 和參數，並傳遞 `op` 或的 `Between` 值 `NotBetween`。

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| ` *`欄位`*` | `xsd:string` | 「資產搜尋系統」欄位選擇。 |
| ` *`op`*` | `xsd:string` | 字串比較運算子的選擇。 |
| ` *`值`*` | `xsd:string` | 要測試的值。 |
| ` *`boolVal`*` | `xsd:boolean` | 布林值比較值。 |
| ` *`longVal`*` | `xsd:long` | 長比較值。 |
| ` *`minLong`*` | `xsd:long` | 遠程下界。 |
| ` *`maxLong`*` | `xsd:long` | 長程上界。 |
| ` *`doubleVal`*` | `xsd:double` | 雙重比較值。 |
| ` *`minDouble`*` | `xsd:double` | 雙程下界。 |
| ` *`maxDouble`*` | `xsd:double` | 雙程上界。 |
| ` *`dateVal`*` | `xsd:dateTime` | 日期比較值。 |
| ` *`minDate`*` | `xsd:dateTime` | 日期範圍小。 |
| ` *`maxDate`*` | `xsd:dateTime` | 日期範圍上限。 |

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

