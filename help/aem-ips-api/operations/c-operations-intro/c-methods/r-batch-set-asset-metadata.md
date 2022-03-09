---
description: 使用批模式設定資產元資料。
solution: Experience Manager
title: batchSetAssetMetadata
feature: Dynamic Media Classic,SDK/API,Metadata,Asset Management
role: Developer,Admin
exl-id: 7393fa4f-71fb-48a5-a7f3-91eec82c88c1
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 13%

---

# batchSetAssetMetadata{#batchsetassetmetadata}

使用批模式設定資產元資料。

語法

## 授權用戶類型 {#section-5310d9fd00604cbf9756944900378855}

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
| 公司句柄 | `xsd:string` | 是 | 要在批處理操作中設定其元資料的公司的句柄。 |
| 更新陣列 | `types:BatchMetadataUpdateArray` | 是 | 應用於資產的元資料更新陣列。 |

**輸出(batchSetAssetMetadataParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 成功計數 | `xsd:int` | 是 | 成功設定元資料的數量。 |
| 警告計數 | `xsd:int` | 是 | 嘗試設定元資料時生成的警告數。 |
| 錯誤計數 | `xsd:int` | 是 | 嘗試設定元資料時生成的錯誤數。 |
| 警告DetailArray | `types:AssetOperationFaultArray` | 否 | 當操作嘗試批處理設定資產的元資料時，與資產關聯的詳細資訊陣列生成警告。 |
| 錯誤DetailArray | `types:AssetOperationFaultArray` | 否 | 與在操作嘗試為資產批處理設定元資料時生成錯誤的資產關聯的詳細資訊陣列。 |

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
