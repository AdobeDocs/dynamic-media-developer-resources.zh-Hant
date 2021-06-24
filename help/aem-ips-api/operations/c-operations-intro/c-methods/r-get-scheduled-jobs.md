---
description: 獲取計畫運行的作業。
solution: Experience Manager
title: getScheduledJobs
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 7920637e-b289-410c-ae5c-e67cd7b21aba
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 21%

---

# getScheduledJobs{#getscheduledjobs}

獲取計畫運行的作業。

語法

## 授權的使用者類型 {#section-bd1835ab508a429f8143b3bdb811d6a4}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 參數 {#section-2af604ff8282460990b9237158187f8f}

**輸入(getScheduledJobsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 公司的把手。 |
| `*`jobHandle`*` | `xsd:string` | 否 | 工作處理。 |
| `*`originalName`*` | `xsd:string` | 否 | 由`submitJob`指定的名稱。 |

**輸出(getScheduledJobsReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`jobArray`*` | `types:ScheduledJobArray` | 是 | 排程作業的陣列。 |

## 範例 {#section-e79e7da86ba848fd9996aa36de462e6c}

此程式碼範例會傳回作業陣列中所有已排程的作業。 陣列本身包含有關作業的詳細資訊。

**請求**

```java
<getScheduledJobsParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>0</companyHandle>
</getScheduledJobsParam>
```

**回答**

```java
<getScheduledJobsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <jobArray>
      <items>
         <companyHandle>0</companyHandle>
         <jobHandle>0|Cleanup|</jobHandle>
         <name>Cleanup</name>
         <originalName></originalName>
         <type>Cleanup</type>
         <submitUserEmail>default@scene7.com</submitUserEmail>
         <execSchedule>00 00 00 * * </execSchedule>
         <nextFireTime>2007-10-13T00:00:00.000-07:00</nextFireTime>
         <timeZone>PST</timeZone>
         <triggerState>Paused</triggerState>
      </items>
   </jobArray>
</getScheduledJobsReturn>
```
