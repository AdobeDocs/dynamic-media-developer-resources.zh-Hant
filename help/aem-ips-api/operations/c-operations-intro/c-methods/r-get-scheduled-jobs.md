---
description: 獲取計畫運行的作業。
seo-description: 獲取計畫運行的作業。
seo-title: getScheduledJobs
solution: Experience Manager
title: getScheduledJobs
topic: Dynamic Media Image Production System API
uuid: 56b0623b-46d7-4d11-8eea-6543ed364b53
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 20%

---


# getScheduledJobs{#getscheduledjobs}

獲取計畫運行的作業。

語法

## 授權用戶類型{#section-bd1835ab508a429f8143b3bdb811d6a4}

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
| `*`jobHandle`*` | `xsd:string` | 否 | 工作代理。 |
| `*`originalName`*` | `xsd:string` | 否 | `submitJob`指定的名稱。 |

**輸出(getScheduledJobsReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`jobArray`*` | `types:ScheduledJobArray` | 是 | 排程作業的陣列。 |

## 範例 {#section-e79e7da86ba848fd9996aa36de462e6c}

此代碼示例返回作業陣列中的所有已調度作業。 陣列本身包含有關作業的詳細資訊。

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

