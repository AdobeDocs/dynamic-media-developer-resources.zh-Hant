---
description: 設定ICC設定檔中繼資料欄位。
solution: Experience Manager
title: batchSetIccProfield
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d10a30ca-afa7-4ef0-8cef-0329b0068bf3
TQID: 'https://experienceleague.adobe.com/YmeLGJ9N-W-JOU7oG7utN4d1Q2pV17wtqocdrwYD-lQ'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 137
ht-degree: 13%

---

# batchSetIccProfield{#batchseticcprofilefields}

設定ICC設定檔中繼資料欄位。

語法

## 授權的使用者型別 {#section-f6f7caf9434b4f469518dab64b76c0f4}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 參數 {#section-75a02b55ae0d444ca26b59aac6e86d6f}

**輸入(batchSetIccProfileFields)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 處理包含ICC設定檔的公司。 |
| 更新陣列 | `xsd:string` | 是 | ICC設定檔更新的陣列。 |

**輸出(batchSetIccProfileFields)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| successCount | `xsd:int` | 是 | 成功設定ICC設定檔欄位的數量。 |
| warningcount | `xsd:int` | 是 | 作業嘗試設定ICC設定檔欄位時產生的警告數目。 |
| errororcount | `xsd:int` | 是 | 作業嘗試設定ICC設定檔欄位時產生的錯誤數目。 |
| warningDetailArray | `types:AssetOperationFaultArray` | 否 | 與資產關聯的詳細資訊陣列，在作業嘗試套用更新時產生警告。 |
| errorDetailArray | `types:AssetOperationFaultArray` | 否 | 與資產關聯的詳細資訊陣列，在操作嘗試套用更新時產生錯誤。 |

## 範例 {#section-5dc90cfbd9b1411485b44859032f7cb9}

**要求**

```java {.line-numbers}
<batchSetIccProfileFieldsParam xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <companyHandle>c|1</companyHandle>
   <updateArray>
      <items>
         <assetHandle>a|1808|13|169</assetHandle>
         <class>Output</class>
         <colorSpace>CMYK</colorSpace>
         <pcsType>Luv</pcsType>
      </items>
   </updateArray>
</batchSetIccProfileFieldsParam>
```

**回應**

```java {.line-numbers}
<batchSetIccProfileFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</batchSetIccProfileFieldsReturn>
```
