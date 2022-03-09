---
description: 根據傳入的參數返回2種不同類型的資訊。 originatorHandle返回有關從指定資產生成的資產的資訊。 generateHandle返回有關用於生成指定資產或檔案的步驟的資訊。
solution: Experience Manager
title: getGenerationInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fa098e3c-8145-4238-a84c-c545f1c53341
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 10%

---

# getGenerationInfo{#getgenerationinfo}

根據傳入的參數返回2種不同類型的資訊。 originatorHandle返回有關從指定資產生成的資產的資訊。 generateHandle返回有關用於生成指定資產或檔案的步驟的資訊。

語法

## 授權用戶類型 {#section-9cc2216b32c74107be07aeacecc11401}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 參數 {#section-b7fa94c82147455888e8469fa5f6922b}

**輸入(getGenerationInfoParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 代碼短語 | `xsd:string` | 是 | 公司的把手。 |
| 代碼短語 | `xsd:string` | 否 | 那個在這代人中使用的引擎。 請參閱字型樣式。 |
| 代碼短語 | `xsd:string` | 否 | 要查詢生成的資產的句柄。 |
| 代碼短語 | `xsd:string` | 否 | 要查詢其生成中使用的資產和引擎的資產句柄。 |
| 代碼短語 | `xsd:StringArray` | 否 | 操作中包含的屬性。 |
| 代碼短語 | `xsd:StringArray` | 否 | 從操作中排除的屬性。 |

**輸出(getGenerationInfoReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| generationArray | `types:GenerationInfoArray` | 是 | 層代資訊的陣列。 |

## 範例 {#section-fdffe6ed82d94c7aa90e47f7ce889403}

此代碼示例返回有關從特定資產生成的資產的資訊。 它不會檢索有關用於生成指定資產的步驟的資訊。 響應被截斷以便簡化。

**請求**

```java
<getGenerationInfoParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <originatorHandle>a|716|25|160</originatorHandle>
</getGenerationInfoParam>
```

**回答**

```java
<getGenerationInfoReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <generationArray>
      <items>
         <engine>PostScriptRip</engine>
         <originator>
         ...
         </generated>
         <attributeArray/>
      </items>
   </generationArray>
</getGenerationInfoReturn>
```
