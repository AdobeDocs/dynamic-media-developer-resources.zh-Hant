---
description: 獲取所選公司的指定作業日誌。 可以按字元、方向、開始和結束日期以及行數排序。
solution: Experience Manager
title: getJobLogs
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 6239c3c4-bdbc-4e69-82d4-48a76f080eff
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 11%

---

# getJobLogs{#getjoblogs}

獲取所選公司的指定作業日誌。 可以按字元、方向、開始和結束日期以及行數排序。

語法

## 授權用戶類型 {#section-9df82972265d44c9ad91504a17c3ffa6}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 參數 {#section-8cfdc7994da24678a45edcb37e9a2166}

**輸入(getJobLogsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 公司句柄 | `xsd:string` | 否 | 公司負責。 |
| userHandle | `xsd:string` | 否 | 獲取特定用戶提交的作業的日誌。 |
| 排序依據 | `xsd:string` | 否 | 用於選擇排序欄位。 |
| 排序方向 | `xsd:string` | 否 | 排序順序（升序或降序）。 |
| 開始日期 | `xsd:dateTime` | 否 | 作業日誌開始的日期和時間。 為時區提供此欄位的請求。 |
| 結束日期 | `xsd:dateTime` | 否 | 作業日誌結束的日期和時間。 為時區提供此欄位的請求。 |
| 行數 | `xsd:int` | 否 | 要返回的最大行數。 |

**輸出(getJobLogsReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 作業日誌陣列 | `types: JobLogArray` | 是 | 作業日誌的陣列。 |

## 範例 {#section-35871c94b4a44559912577efddbc46a6}

此代碼示例返回特定公司的IPS作業日誌。 您還可以使用它返回特定用戶或公司和用戶的作業日誌。

**請求**

```java
<ns1:getJobLogsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getJobLogsParam>
```

**回答**

```java
<getJobLogsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <jobLogArray>
      <items>
         <companyHandle>47</companyHandle>
         <jobHandle>47||Add_2007-09-14-15:04:34</jobHandle>
         <jobName>Add_2007-09-14-15:04:34</jobName>
         <submitUserEmail>kmagnusson@adobe.com</submitUserEmail>
         <logType>BeginUpload</logType>
         <startDate>2007-09-14T22:04:58.536-07:00</startDate>
         <fileSuccessCount>2</fileSuccessCount>
         <fileErrorCount>0</fileErrorCount>
         <fileWarningCount>205</fileWarningCount>
         <fileDuplicateCount>0</fileDuplicateCount>
         <fileUpdateCount>0</fileUpdateCount>
         <totalFileCount>0</totalFileCount>
         <fatalError>false</fatalError>
       </items>
   </jobLogArray>
</getJobLogsReturn>
```
