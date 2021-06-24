---
description: 根據傳入的參數傳回2種不同的資訊。 originator處理返回有關從指定資產生成的資產的資訊。 generateHandle返回有關用於生成指定資產或檔案的步驟的資訊。
solution: Experience Manager
title: getGenerationInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: fa098e3c-8145-4238-a84c-c545f1c53341
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 9%

---

# getGenerationInfo{#getgenerationinfo}

根據傳入的參數傳回2種不同的資訊。 originator處理返回有關從指定資產生成的資產的資訊。 generateHandle返回有關用於生成指定資產或檔案的步驟的資訊。

語法

## 授權的使用者類型 {#section-9cc2216b32c74107be07aeacecc11401}

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
| `*`代碼片語`*` | `xsd:string` | 是 | 公司的把手。 |
| `*`代碼片語`*` | `xsd:string` | 否 | 那代人用的引擎。 請參閱字型樣式。 |
| `*`代碼片語`*` | `xsd:string` | 否 | 要查詢所產生資產的資產處理。 |
| `*`代碼片語`*` | `xsd:string` | 否 | 要查詢用於產生資產和引擎的資產處理。 |
| `*`代碼片語`*` | `xsd:StringArray` | 否 | 操作中包含的屬性。 |
| `*`代碼片語`*` | `xsd:StringArray` | 否 | 從操作中排除的屬性。 |

**輸出(getGenerationInfoReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`generationArray`*` | `types:GenerationInfoArray` | 是 | 生成資訊的陣列。 |

## 範例 {#section-fdffe6ed82d94c7aa90e47f7ce889403}

此程式碼範例會傳回從特定資產產生的資產相關資訊。 它不會擷取用於產生指定資產之步驟的相關資訊。 回應會為簡潔而截斷。

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
