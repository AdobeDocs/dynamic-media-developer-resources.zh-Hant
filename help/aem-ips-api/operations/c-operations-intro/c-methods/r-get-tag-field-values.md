---
description: 取得針對一或多個標籤欄位定義的所有標籤字典值。
solution: Experience Manager
title: getTagFieldValue
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 12836783-4f9d-41d3-9b42-6e25238d7ed5
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 16%

---

# getTagFieldValue{#gettagfieldvalues}

取得針對一或多個標籤欄位定義的所有標籤字典值。

語法

## 授權的使用者型別 {#section-cc36a437394c491594e704a08a161c87}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 參數 {#section-9ad806e7736e4d51ae42cad185050cf9}

**輸入(getTagFieldValuesReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 包含標籤欄位之公司的控制代碼。 |
| fieldHandleArray | `types:HandleArray` | 是 | 用於標籤要傳回之值的欄位控制代碼陣列。 |

**輸出(getTagFieldValuesReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| fieldArray | `types:TagFieldValuesArray` | 是 | 字典中每個請求欄位的標籤值陣列。 |

## 範例 {#section-4492742614e44bb191a7d397dc1a1407}

**要求**

```java
<getTagFieldValuesParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <fieldHandleArray>
      <items>m|3|ASSET|SingleOpenTag</items>
      <items>m|3|ASSET|SingleFixedTag</items>
   </fieldHandleArray>
</getTagFieldValuesParam>
```

**回應**

```java
<getTagFieldValuesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <fieldArray>
      <items>
         <fieldHandle>m|3|ASSET|SingleOpenTag</fieldHandle>
         <valueArray>
            <items>GroupB</items>
            <items>GroupA</items>
         </valueArray>
      </items>
      <items>
         <fieldHandle>m|3|ASSET|SingleFixedTag</fieldHandle>
         <valueArray>
            <items>North</items>
            <items>South</items>
            <items>East</items><items>West</items>
         </valueArray>
      </items>
   </fieldArray>
</getTagFieldValuesReturn>
```
