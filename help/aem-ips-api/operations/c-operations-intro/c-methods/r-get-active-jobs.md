---
description: 獲取所有當前活動作業。
solution: Experience Manager
title: getActiveJobs
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 55e92ebc-d153-49b5-bf2e-c69d042e15b6
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 16%

---

# getActiveJobs{#getactivejobs}

獲取所有當前活動作業。

語法

## 授權的使用者類型 {#section-125557a6ea7b4fc894d4bb468cd02118}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 參數 {#section-29018fba6bf34c1e80dcd479dd24f3b5}

**輸入(getActiveJobsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 否 | 公司的把手。 |
| `*`jobHandle`*` | `xsd:string` | 否 | 工作的控制。 |
| `*`originalName`*` | `xsd:string` | 否 | 原始作業名稱。 |

**輸出(getActiveJobsReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`jobArray`*` | `xsd:string` | 是 | 活動作業的陣列。 |

## 範例 {#section-4ac5dbbf9cd94fdeb013d055f8ee7add}

此代碼示例返回在IPS中運行的公司的所有活動作業。 在這種情況下，響應異常，因為IPS調度協調器被禁用，且沒有運行活動作業。 在正常情況下，回應會傳回數個作用中工作。

**請求**

```java
<ns1:getActiveJobsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getActiveJobsParam>
```

**回答**

```java
<getActiveJobsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <jobArray></jobArray>
</getActiveJobsReturn>
```
