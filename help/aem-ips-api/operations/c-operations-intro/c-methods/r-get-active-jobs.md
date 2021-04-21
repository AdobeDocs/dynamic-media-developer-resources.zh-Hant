---
description: 獲取所有當前活動的作業。
solution: Experience Manager
title: getActiveJobs
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 15%

---


# getActiveJobs{#getactivejobs}

獲取所有當前活動的作業。

語法

## 授權用戶類型{#section-125557a6ea7b4fc894d4bb468cd02118}

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
| `*`originalName`*` | `xsd:string` | 否 | 原始工作名稱。 |

**輸出(getActiveJobsReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`jobArray`*` | `xsd:string` | 是 | 活動作業的陣列。 |

## 範例 {#section-4ac5dbbf9cd94fdeb013d055f8ee7add}

此代碼示例返回在IPS中運行的公司的所有活動作業。 在這種情況下，響應異常，因為IPS調度協調器處於禁用狀態，且沒有運行活動作業。 在正常情況下，回應會傳回許多作用中的工作。

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

