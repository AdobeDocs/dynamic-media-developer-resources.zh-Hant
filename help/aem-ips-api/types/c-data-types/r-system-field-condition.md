---
description: searchAssets作業的系統欄位搜尋條件。
solution: Experience Manager
title: SystemFieldCondition
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: ebd12727-dbb3-40dc-b631-945415331be6
TQID: 'https://experienceleague.adobe.com/dCZl4pLGuG5hHpEq04W-qv8mRWcFiA7PvmzcO7Un-sM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 83717f155466c1b33cab6f1f8830a9fea68c88c5
workflow-type: tm+mt
source-wordcount: 116
ht-degree: 6%

---

# [!DNL SystemFieldCondition]{#systemfieldcondition}

searchAssets作業的系統欄位搜尋條件。

若要一元比較，請根據系統欄位型別，僅傳遞一個值（ `boolVal`、`longVal`、`doubleVal`或`dateVal`）。 針對搜尋範圍，傳遞`min<Type>`和`max<Type>`引數，並傳遞`Between`或`NotBetween`的`op`值。

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| 欄位 | `xsd:string` | 資產搜尋系統欄位的選擇。 |
| op | `xsd:string` | 字串比較運運算元的選擇。 |
| 價值 | `xsd:string` | 要測試的值。 |
| boolVal | `xsd:boolean` | 布林值比較值。 |
| longVal | `xsd:long` | 長比較值。 |
| minLong | `xsd:long` | 長範圍的下限。 |
| maxLong | `xsd:long` | 長範圍的上限。 |
| doubleVal | `xsd:double` | 雙倍比較值。 |
| minDouble | `xsd:double` | 雙精度範圍下限。 |
| maxDouble | `xsd:double` | 雙精度範圍的上限。 |
| 日期值 | `xsd:dateTime` | 日期比較值。 |
| minDate | `xsd:dateTime` | 日期範圍下限。 |
| maxDate | `xsd:dateTime` | 日期範圍上限。 |

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

