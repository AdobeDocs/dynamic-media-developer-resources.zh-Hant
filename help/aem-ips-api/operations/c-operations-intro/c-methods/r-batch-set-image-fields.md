---
description: 設定一或多個影像資產的影像特定欄位。
solution: Experience Manager
title: batchSetImageField
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 8ea6dbb8-4d32-43e5-961f-31110f983663
TQID: 'https://experienceleague.adobe.com/J3mCGBUY4Ws5Wq18tHWrHQJNElW5gYvwSQ2yKF-NhsM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 195
ht-degree: 9%

---

# batchSetImageField{#batchsetimagefields}

設定一或多個影像資產的影像特定欄位。

語法

## 授權的使用者型別 {#section-6b087bdcb7874c13acf76e113a093054}

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
| companyHandle | `xsd:string` | 是 | 包含影像資產之公司的控制代碼。 |
| updatearray | `types:ImageFieldUpdateArray` | 是 | 影像欄位更新的陣列。 |

**輸出(batchSetImageFields)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| successCount | `xsd:int` | 是 | 已成功設定影像欄位的數量。 |
| warningcount | `xsd:int` | 是 | 作業嘗試設定影像欄位時產生的警告數目。 |
| errororcount | `xsd:int` | 是 | 作業嘗試設定影像欄位時產生的錯誤數目。 |
| warningDetailArray | `types:AssetOperationFaultArray` | 否 | 與資產關聯的詳細資訊陣列，在作業嘗試套用更新時產生警告。 |
| errorDetailArray | `types:AssetOperationFaultArray` | 否 | 與資產關聯的詳細資訊陣列，在操作嘗試套用更新時產生錯誤。 |

## 範例 {#section-0476e3d6516a4f8bbaac9de983bc6d1e}

此範例會在更新陣列中設定兩個影像欄位中的資料。 在陣列中，影像由其資產控點指定，並包含解析度（畫素）、x和y位置錨點座標和使用者資料。 此回應表示兩個影像的欄位都已成功設定。

**要求**

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

**回應**

```java
<batchSetImageFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</batchSetImageFieldsReturn>
```
