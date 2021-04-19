---
description: 使用批次模式設定資產中繼資料。
solution: Experience Manager
title: batchSetAssetMetadata
feature: Dynamic Media經典，SDK/API，元資料，資產管理
role: Developer,Administrator
exl-id: 7393fa4f-71fb-48a5-a7f3-91eec82c88c1
translation-type: tm+mt
source-git-commit: f464a7adcb8035a5bdebf1a6c9b647ba04535431
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 13%

---

# batchSetAssetMetadata{#batchsetassetmetadata}

使用批次模式設定資產中繼資料。

語法

## 授權用戶類型{#section-5310d9fd00604cbf9756944900378855}

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
| `*`companyHandle`*` | `xsd:string` | 是 | 要在批處理操作中設定其元資料的公司的句柄。 |
| `*`updateArray`*` | `types:BatchMetadataUpdateArray` | 是 | 套用至資產的中繼資料更新陣列。 |

**輸出(batchSetAssetMetadataParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | 是 | 成功設定中繼資料的數目。 |
| `*`warningCount`*` | `xsd:int` | 是 | 嘗試設定中繼資料時產生的警告數。 |
| `*`errorCount`*` | `xsd:int` | 是 | 嘗試設定中繼資料時產生的錯誤數。 |
| `*`warningDetailArray`*` | `types:AssetOperationFaultArray` | 否 | 當操作嘗試批次設定資產的中繼資料時，與資產相關的詳細資料陣列會產生警告。 |
| `*`errorDetailArray`*` | `types:AssetOperationFaultArray` | 否 | 當操作嘗試為資產批次設定中繼資料時，與產生錯誤的資產相關聯的詳細資料陣列。 |

## 範例 {#section-2de798ac920e4b47b971b1729a64395b}

**請求**

```java
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

**回答**

```java
<batchSetAssetMetadataReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>4</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</batchSetAssetMetadataReturn>
```
