---
description: searchAssets操作的系統欄位搜索條件。
solution: Experience Manager
title: 系統欄位條件
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: ebd12727-dbb3-40dc-b631-945415331be6
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 6%

---

# 系統欄位條件{#systemfieldcondition}

searchAssets操作的系統欄位搜索條件。

對於一元比較，只傳遞一個值( `boolVal`。 `longVal`。 `doubleVal`或 `dateVal`)，具體取決於系統欄位類型。 對於搜索範圍，傳遞 `min<Type>` 和 `max<Type>` 參數並傳遞 `op` 值 `Between` 或 `NotBetween`。

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| 欄位 | `xsd:string` | 「資產搜索系統」欄位的選擇。 |
| op | `xsd:string` | 字串比較運算子的選擇。 |
| 價值 | `xsd:string` | 對其test的值。 |
| 布爾瓦爾 | `xsd:boolean` | 布爾比較值。 |
| 朗瓦爾 | `xsd:long` | 比較值較長。 |
| 閩龍 | `xsd:long` | 長程下界。 |
| 最大長度 | `xsd:long` | 遠程上界。 |
| 雙谷 | `xsd:double` | 雙重比較值。 |
| 最小雙倍 | `xsd:double` | 雙範圍下界。 |
| 最大雙倍 | `xsd:double` | 雙範圍上界。 |
| 日期值 | `xsd:dateTime` | 日期比較值。 |
| 最小日期 | `xsd:dateTime` | 日期範圍小。 |
| 最大日期 | `xsd:dateTime` | 日期範圍最大值。 |

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
