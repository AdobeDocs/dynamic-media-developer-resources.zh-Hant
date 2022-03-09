---
description: 獲取資產的作業日誌。 陣列中返回的項目包含有關該資產的作業日誌中每個條目的詳細資訊。 日誌消息響應欄位基於authHeader欄位進行本地化。
solution: Experience Manager
title: getAssetJobLogs
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 88ec5cab-7eb4-48aa-914f-21311593e463
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 10%

---

# getAssetJobLogs{#getassetjoblogs}

獲取資產的作業日誌。 陣列中返回的項目包含有關該資產的作業日誌中每個條目的詳細資訊。 日誌消息響應欄位基於authHeader欄位進行本地化。

語法

## 授權用戶類型 {#section-72b98cdb0f6f47f5aabdc183a45ea577}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 參數 {#section-9586617e124b4da4acb6b66b2a9adad8}

**輸入(getAssetJobLogsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 公司句柄 | `xsd:string` | 是 | 資產所屬公司的句柄。 |
| 資產句柄 | `xsd:string` | 是 | 要與要檢索的作業日誌一起進行資產的句柄。 |

**輸出(getAssetJobLogsReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 作業日誌陣列 | `types:AssetJobLogArray` | 是 | 作業日誌陣列。 |

## 範例 {#section-f03d7f3ec5d043d38227f926fb7609f6}

此代碼示例檢索特定資產的作業日誌。 該響應返回一個作業日誌陣列，其中包含有關使用該資產的所有作業的詳細資訊。

**請求**

```java
<getAssetJobLogsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandle>a|732|1|535</assetHandle>
</getAssetJobLogsParam>
```

**回答**

```java
<getAssetJobLogsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <jobLogArray>
      <items>
         <jobHandle>j|6||Add_2007-10-24-16:11:07</jobHandle>
         <jobName>Add_2007-10-24-16:11:07</jobName>
         <logMessage>ApiTestCo/blakexslttest.jpg was processed into IPS</logMessage>
         <logType>UploadSuccess</logType>
         <submitUserEmail>strangio@adobe.com</submitUserEmail>
         <logDate>2007-10-24T16:12:32.297-07:00</logDate>
      </items>
      <items>
         <jobHandle>j|6||submitServerUploadJob40_2008-06-11-11:38</jobHandle>
         <jobName>submitServerUploadJob40_2008-06-11-11:38</jobName>
         <logMessage>ApiTestCo/blakexslttest.jpg was processed into IPS.</logMessage>
         <logType>FileUpdated</logType>
         <submitUserEmail>strangio@adobe.com</submitUserEmail>
         <logDate>2008-06-11T11:38:48.547-07:00</logDate>
      </items>
   </jobLogArray>
</getAssetJobLogsReturn>
```
