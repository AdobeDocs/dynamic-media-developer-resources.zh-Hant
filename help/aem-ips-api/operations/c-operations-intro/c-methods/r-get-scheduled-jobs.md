---
description: 獲取計畫運行的作業。
solution: Experience Manager
title: getScheduledJobs
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 7920637e-b289-410c-ae5c-e67cd7b21aba
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 22%

---

# getScheduledJobs{#getscheduledjobs}

獲取計畫運行的作業。

語法

## 授權用戶類型 {#section-bd1835ab508a429f8143b3bdb811d6a4}

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
| 公司句柄 | `xsd:string` | 是 | 公司的把手。 |
| 作業句柄 | `xsd:string` | 否 | 作業處理。 |
| 原始名稱 | `xsd:string` | 否 | 指定的名稱 `submitJob`。 |

**輸出(getScheduledJobsReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| jobArray | `types:ScheduledJobArray` | 是 | 計畫的作業陣列。 |

## 範例 {#section-e79e7da86ba848fd9996aa36de462e6c}

此代碼示例返回作業陣列中的所有計畫作業。 陣列本身包含有關作業的詳細資訊。

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
