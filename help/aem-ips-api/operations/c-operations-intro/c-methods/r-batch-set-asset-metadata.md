---
description: 使用批次模式設定資產中繼資料。
solution: Experience Manager
title: batchSetAssetMetadata
feature: Dynamic Media Classic,SDK/API,Metadata,Asset Management
role: Developer,Admin
exl-id: 7393fa4f-71fb-48a5-a7f3-91eec82c88c1
TQID: 'https://experienceleague.adobe.com/MQA1ShXDX9EUPfR9LolEVhA6F52W71gGZI75miE7uRs'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 4185012f22b173b569d11ea4d350763a82f98710
workflow-type: tm+mt
source-wordcount: 145
ht-degree: 12%

---

# batchSetAssetMetadata{#batchsetassetmetadata}

使用批次模式設定資產中繼資料。

語法

## 授權的使用者型別 {#section-5310d9fd00604cbf9756944900378855}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 參數 {#section-7111ac93bc7747f69ba14db4ac3912b0}

**輸入(batchSetAssetMetadataParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 要在批次作業中設定中繼資料之公司的控制代碼。 |
| updatearray | `types:BatchMetadataUpdateArray` | 是 | 套用至資產的中繼資料更新陣列。 |

**輸出(batchSetAssetMetadataParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| successCount | `xsd:int` | 是 | 已成功設定中繼資料的數目。 |
| warningcount | `xsd:int` | 是 | 作業嘗試設定中繼資料時產生的警告數目。 |
| errororcount | `xsd:int` | 是 | 作業嘗試設定中繼資料時產生的錯誤數。 |
| warningDetailArray | `types:AssetOperationFaultArray` | 否 | 與資產關聯的詳細資訊陣列，在操作嘗試批次設定資產的中繼資料時產生警告。 |
| errorDetailArray | `types:AssetOperationFaultArray` | 否 | 與資產關聯的詳細資訊陣列，這些詳細資訊會在操作嘗試批次設定資產的中繼資料時產生錯誤。 |

## 範例 {#section-2de798ac920e4b47b971b1729a64395b}

**要求**

```java {.line-numbers}
<batchSetAssetMetadataParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
<companyHandle>c|6</companyHandle>
<updateArray>
   <items>
      <assetHandleArray>
         <items>a|743|1|538</items>
         <items>a|744|1|539</items>
      </assetHandleArray>
      <updateArray>
         <items>
            <fieldHandle>m|6|IMAGE|saveMetadataField</fieldHandle>
            <value>400</value>
         </items>
      </updateArray>
   </items>
   <items>
      <assetHandleArray>
         <items>a|732|1|535</items>
         <items>a|739|1|537</items>
      </assetHandleArray>
      <updateArray>
         <items>
            <fieldHandle>m|6|IMAGE|saveMetadataField</fieldHandle>
            <value>300</value>
         </items>
      </updateArray>
   </items>
</updateArray>
</batchSetAssetMetadataParam>
```

**回應**

```java {.line-numbers}
<batchSetAssetMetadataReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>4</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</batchSetAssetMetadataReturn>
```

