---
description: 取得所選公司的指定工作記錄檔。 您可以依字元、方向、開始和結束日期以及列數排序。
solution: Experience Manager
title: getJobLogs
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 6239c3c4-bdbc-4e69-82d4-48a76f080eff
TQID: 'https://experienceleague.adobe.com/lerbQ3ibPCI3zqkrmgPrwTAYp1w6dWxIWYRt2Ij51oA'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 184
ht-degree: 10%

---

# getJobLogs{#getjoblogs}

取得所選公司的指定工作記錄檔。 您可以依字元、方向、開始和結束日期以及列數排序。

語法

## 授權的使用者型別 {#section-9df82972265d44c9ad91504a17c3ffa6}

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
| companyHandle | `xsd:string` | 否 | 公司控制代碼。 |
| userHandle | `xsd:string` | 否 | 取得特定使用者所提交工作的記錄。 |
| sortBy | `xsd:string` | 否 | 可讓您選取排序欄位。 |
| sortDirection | `xsd:string` | 否 | 排序順序（升序或降序）。 |
| startDate | `xsd:dateTime` | 否 | 工作記錄檔的開始日期和時間。 提供此欄位要求的時區。 |
| endDate | `xsd:dateTime` | 否 | 工作記錄結束的日期和時間。 提供此欄位要求的時區。 |
| numRows | `xsd:int` | 否 | 要傳回的最大列數。 |

**輸出(getJobLogsReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| jobLogArray | `types: JobLogArray` | 是 | 工作記錄陣列。 |

## 範例 {#section-35871c94b4a44559912577efddbc46a6}

此程式碼範例會傳回特定公司的IPS工作記錄檔。 您也可以用它來傳回特定使用者、公司和使用者的工作記錄檔。

**要求**

```java
<ns1:getJobLogsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getJobLogsParam>
```

**回應**

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

