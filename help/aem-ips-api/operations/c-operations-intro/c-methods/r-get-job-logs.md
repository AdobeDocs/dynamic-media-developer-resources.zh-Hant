---
description: 獲取所選公司的指定作業日誌。 您可以依字元、方向、開始和結束日期以及列數來排序。
solution: Experience Manager
title: getJobLogs
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 10%

---


# getJobLogs{#getjoblogs}

獲取所選公司的指定作業日誌。 您可以依字元、方向、開始和結束日期以及列數來排序。

語法

## 授權用戶類型{#section-9df82972265d44c9ad91504a17c3ffa6}

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
| `*`companyHandle`*` | `xsd:string` | 否 | 公司負責人。 |
| `*`userHandle`*` | `xsd:string` | 否 | 獲取特定用戶提交的作業的日誌。 |
| `*`sortBy`*` | `xsd:string` | 否 | 可讓您選取排序欄位。 |
| `*`sortDirection`*` | `xsd:string` | 否 | 排序順序（遞增或遞減）。 |
| `*`startDate`*` | `xsd:dateTime` | 否 | 作業日誌開始的日期和時間。 為時區提供此欄位的請求。 |
| `*`endDate`*` | `xsd:dateTime` | 否 | 作業日誌結束的日期和時間。 為時區提供此欄位的請求。 |
| `*`numRows`*` | `xsd:int` | 否 | 要返回的最大行數。 |

**輸出(getJobLogsReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`jobLogArray`*` | `types: JobLogArray` | 是 | 作業日誌的陣列。 |

## 範例 {#section-35871c94b4a44559912577efddbc46a6}

此程式碼範例會傳回特定公司的IPS工作記錄檔。 您也可以使用它來傳回特定使用者、公司及使用者的工作記錄檔。

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

