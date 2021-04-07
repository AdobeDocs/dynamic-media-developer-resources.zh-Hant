---
description: 為一或多個影像資產設定影像特定欄位。
solution: Experience Manager
title: batchSetImageFields
feature: Dynamic Media經典，SDK/API
role: 開發人員、管理員
exl-id: 8ea6dbb8-4d32-43e5-961f-31110f983663
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 10%

---

# batchSetImageFields{#batchsetimagefields}

為一或多個影像資產設定影像特定欄位。

語法

## 授權用戶類型{#section-6b087bdcb7874c13acf76e113a093054}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 參數 {#section-4969815cf67c4d11b13bb2017b3604e8}

**輸入(batchSetImageFields)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 包含影像資產之公司的控制代碼。 |
| `*`updateArray`*` | `types:ImageFieldUpdateArray` | 是 | 影像欄位陣列會更新。 |

**輸出(batchSetImageFields)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | 是 | 成功設定影像欄位的數目。 |
| `*`warningCount`*` | `xsd:int` | 是 | 嘗試設定影像欄位時產生的警告數。 |
| `*`errorCount`*` | `xsd:int` | 是 | 嘗試設定影像欄位時產生的錯誤數。 |
| `*`warningDetailArray`*` | `types:AssetOperationFaultArray` | 否 | 與資產相關的詳細資訊陣列，當操作嘗試套用更新時，這些資產會產生警告。 |
| `*`errorDetailArray`*` | `types:AssetOperationFaultArray` | 否 | 當操作嘗試套用更新時，與產生錯誤的資產相關的詳細資訊陣列。 |

## 範例 {#section-0476e3d6516a4f8bbaac9de983bc6d1e}

此示例在更新陣列中兩個映像的欄位中設定資料。 在陣列中，影像由其資產控制點指定，並包含像素解析度、x和y位置錨點座標以及使用者資料。 回應表示已成功設定兩個影像的欄位。

**請求**

```java
<batchSetImageFieldsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <updateArray>
      <items>
         <assetHandle>a|140626|1|102524</assetHandle>
         <resolution>72</resolution>
         <anchorX>50</anchorX>
         <anchorY>100</anchorY>
         <userData>nada1</userData>
      </items>
      <items>
         <assetHandle>a|96680|1|64865</assetHandle>
         <resolution>150</resolution>
         <anchorX>100</anchorX>
         <anchorY>50</anchorY>
         <userData>nada2</userData>
      </items>
   </updateArray>
</batchSetImageFieldsParam>
```

**回答**

```java
<batchSetImageFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</batchSetImageFieldsReturn>
```
