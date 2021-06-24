---
description: 設定一或多個資產的縮圖影像。
solution: Experience Manager
title: batchSetThumbAsset
feature: Dynamic Media Classic,SDK/API，資產管理
role: Developer,Administrator
exl-id: f7d7ddd9-a3c3-47c4-8da6-d693851d0d7f
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 13%

---

# batchSetThumbAsset{#batchsetthumbasset}

設定一或多個資產的縮圖影像。

語法

## 縮圖資產類型 {#section-4edc2a6a8f824213b0aaddb1d437268c}

允許的縮圖資產類型包含下列項目：

* 影像
* 調整後的檢視
* 遮色片
* 範本
* Psd模板

## 授權的使用者類型 {#section-5fc988e3d6384968b86fd9fe363658c0}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>使用者必須擁有目標資產的讀/寫存取權，以及縮圖資產的讀取存取權。

## 參數 {#section-9c6efa000b384b3db6c013def20cf40b}

**輸入(batchSetThumbAssetParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 包含資產之公司的控制代碼。 |
| `*`updateArray`*` | `types:ThumbAssetUpdateArray` | 是 | 更新的陣列。 |

**輸出(batchSetThumbAssetParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | 是 | 成功設定縮圖的數量。 |
| `*`warningCount`*` | `xsd:int` | 是 | 操作嘗試設定縮略圖時生成的警告數。 |
| `*`errorCount`*` | `xsd:int` | 是 | 操作嘗試設定縮圖時生成的錯誤數。 |
| `*`warningDetailArray`*` | `types:AssetOperationFaultArray` | 否 | 與資產相關聯的詳細資訊陣列，當操作嘗試套用更新時，資產會產生警告。 |
| `*`errorDetailArray`*` | `types:AssetOperationFaultArray` | 否 | 與嘗試套用更新時產生錯誤之資產相關聯的詳細資訊陣列。 |

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
