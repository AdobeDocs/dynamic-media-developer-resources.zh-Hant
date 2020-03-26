---
description: 獲取為一個或多個標籤欄位定義的所有標籤字典值。
seo-description: 獲取為一個或多個標籤欄位定義的所有標籤字典值。
seo-title: getTagFieldValues
solution: Experience Manager
title: getTagFieldValues
topic: Scene7 Image Production System API
uuid: 92d84dfc-6a6c-4876-9670-1152adb6317c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getTagFieldValues{#gettagfieldvalues}

獲取為一個或多個標籤欄位定義的所有標籤字典值。

語法

## 授權使用者類型 {#section-cc36a437394c491594e704a08a161c87}

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
| ` *`companyHandle`*` | `xsd:string` | 是 | 包含標籤欄位之公司的控制代碼。 |
| ` *`fieldHandleArray`*` | `types:HandleArray` | 是 | 用於標籤要返回值的欄位句柄陣列。 |

**輸出(getTagFieldValuesReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| ` *`fieldArray`*` | `types:TagFieldValuesArray` | 是 | 字典中每個請求欄位的標籤值陣列。 |

## 範例 {#section-4492742614e44bb191a7d397dc1a1407}

**請求**

```java
<getTagFieldValuesParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <fieldHandleArray>
      <items>m|3|ASSET|SingleOpenTag</items>
      <items>m|3|ASSET|SingleFixedTag</items>
   </fieldHandleArray>
</getTagFieldValuesParam>
```

**回答**

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

