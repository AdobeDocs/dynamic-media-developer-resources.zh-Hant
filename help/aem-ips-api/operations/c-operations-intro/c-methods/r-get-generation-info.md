---
description: 根據傳入的參數傳回2種不同的資訊類型。 originatorHandle返回有關從指定資產生成的資產的資訊。 generateHandle返回有關用於生成指定資產或檔案的步驟的資訊。
solution: Experience Manager
title: getGenerationInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 9%

---


# getGenerationInfo{#getgenerationinfo}

根據傳入的參數傳回2種不同的資訊類型。 originatorHandle返回有關從指定資產生成的資產的資訊。 generateHandle返回有關用於生成指定資產或檔案的步驟的資訊。

語法

## 授權用戶類型{#section-9cc2216b32c74107be07aeacecc11401}

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
| `*`程式碼片語`*` | `xsd:string` | 是 | 公司的把手。 |
| `*`程式碼片語`*` | `xsd:string` | 否 | 這代人使用的引擎。 請參閱字型樣式。 |
| `*`程式碼片語`*` | `xsd:string` | 否 | 要查詢已生成資產的資產的句柄。 |
| `*`程式碼片語`*` | `xsd:string` | 否 | 要查詢資產及其生成中使用的資產和引擎的資產句柄。 |
| `*`程式碼片語`*` | `xsd:StringArray` | 否 | 操作中包含的屬性。 |
| `*`程式碼片語`*` | `xsd:StringArray` | 否 | 從操作中排除的屬性。 |

**輸出(getGenerationInfoReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`generationArray`*` | `types:GenerationInfoArray` | 是 | 層代資訊的陣列。 |

## 範例 {#section-fdffe6ed82d94c7aa90e47f7ce889403}

此程式碼範例會傳回特定資產所產生的資產資訊。 它不會擷取有關用來產生指定資產之步驟的資訊。 回應會因簡短而截斷。

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

