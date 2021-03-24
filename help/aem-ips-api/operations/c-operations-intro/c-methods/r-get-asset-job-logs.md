---
description: 取得資產的工作記錄檔。 陣列中返回的項目包含該資產作業日誌中每個條目的詳細資訊。 logMessage響應欄位會根據authHeader欄位本地化。
solution: Experience Manager
title: getAssetJobLogs
feature: Dynamic Media經典，SDK/API，資產管理
role: 開發人員、管理員
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 9%

---


# getAssetJobLogs{#getassetjoblogs}

取得資產的工作記錄檔。 陣列中返回的項目包含該資產作業日誌中每個條目的詳細資訊。 logMessage響應欄位會根據authHeader欄位本地化。

語法

## 授權用戶類型{#section-72b98cdb0f6f47f5aabdc183a45ea577}

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
| `*`companyHandle`*` | `xsd:string` | 是 | 資產所屬公司的控制代碼。 |
| `*`assetHandle`*` | `xsd:string` | 是 | 包含要檢索的作業日誌的資產的句柄。 |

**輸出(getAssetJobLogsReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`jobLogArray`*` | `types:AssetJobLogArray` | 是 | 作業日誌陣列。 |

## 範例 {#section-f03d7f3ec5d043d38227f926fb7609f6}

此程式碼範例會擷取特定資產的工作記錄檔。 該響應返回作業日誌陣列，其中包含使用該資產的所有作業的詳細資訊。

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

