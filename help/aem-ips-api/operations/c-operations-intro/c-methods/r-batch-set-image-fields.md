---
description: 為一個或多個影像資產設定特定於影像的欄位。
solution: Experience Manager
title: batchSetImageFields
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 8ea6dbb8-4d32-43e5-961f-31110f983663
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 10%

---

# batchSetImageFields{#batchsetimagefields}

為一個或多個影像資產設定特定於影像的欄位。

語法

## 授權用戶類型 {#section-6b087bdcb7874c13acf76e113a093054}

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
| 公司句柄 | `xsd:string` | 是 | 包含映像資產的公司的句柄。 |
| 更新陣列 | `types:ImageFieldUpdateArray` | 是 | 映像欄位的陣列更新。 |

**輸出(batchSetImageFields)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 成功計數 | `xsd:int` | 是 | 成功設定影像欄位的數量。 |
| 警告計數 | `xsd:int` | 是 | 嘗試設定影像欄位時生成的警告數。 |
| 錯誤計數 | `xsd:int` | 是 | 嘗試設定影像欄位時生成的錯誤數。 |
| 警告DetailArray | `types:AssetOperationFaultArray` | 否 | 與在操作嘗試應用更新時生成警告的資產關聯的詳細資訊陣列。 |
| 錯誤DetailArray | `types:AssetOperationFaultArray` | 否 | 與在操作嘗試應用更新時生成錯誤的資產關聯的詳細資訊陣列。 |

## 範例 {#section-0476e3d6516a4f8bbaac9de983bc6d1e}

此示例在一個更新陣列中設定兩個映像的欄位中的資料。 在陣列中，影像由其資產句柄指定，並包含以像素、x和y位錨點坐標以及用戶資料為單位的解析度。 響應指示已成功設定兩個影像的欄位。

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
