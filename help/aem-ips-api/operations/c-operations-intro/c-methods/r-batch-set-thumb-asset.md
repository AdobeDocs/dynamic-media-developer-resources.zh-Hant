---
description: 設定一個或多個資產的縮略圖。
solution: Experience Manager
title: batchSetThumbAsset
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: f7d7ddd9-a3c3-47c4-8da6-d693851d0d7f
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 14%

---

# batchSetThumbAsset{#batchsetthumbasset}

設定一個或多個資產的縮略圖。

語法

## 縮略圖資產類型 {#section-4edc2a6a8f824213b0aaddb1d437268c}

允許的縮略圖資產類型包括：

* 影像
* 調整後的檢視
* 遮色片
* 範本
* Psd模板

## 授權用戶類型 {#section-5fc988e3d6384968b86fd9fe363658c0}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>用戶必須具有對目標資產的讀/寫權限和對拇指資產的讀權限。

## 參數 {#section-9c6efa000b384b3db6c013def20cf40b}

**Input(batchSetThumbAssetParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 公司句柄 | `xsd:string` | 是 | 包含資產的公司的句柄。 |
| 更新陣列 | `types:ThumbAssetUpdateArray` | 是 | 更新的陣列。 |

**輸出(batchSetThumbAssetParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 成功計數 | `xsd:int` | 是 | 成功設定縮略圖的數量。 |
| 警告計數 | `xsd:int` | 是 | 嘗試設定縮略圖時生成的警告數。 |
| 錯誤計數 | `xsd:int` | 是 | 嘗試設定縮略圖時生成的錯誤數。 |
| 警告DetailArray | `types:AssetOperationFaultArray` | 否 | 與在操作嘗試應用更新時生成警告的資產關聯的詳細資訊陣列。 |
| 錯誤DetailArray | `types:AssetOperationFaultArray` | 否 | 與在操作嘗試應用更新時生成錯誤的資產關聯的詳細資訊陣列。 |

## 範例 {#section-6de69a8680c24c1486c5f01488393381}

**請求**

```java
<batchSetThumbAssetParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <updateArray>
      <items>
         <assetHandle>a|234</assetHandle>
         <thumbAssetHandle>a|189</thumbAssetHandle>
      </items>
   </updateArray>
```

**回答**

```java
<batchSetThumbAssetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</batchSetThumbAssetReturn>
```
