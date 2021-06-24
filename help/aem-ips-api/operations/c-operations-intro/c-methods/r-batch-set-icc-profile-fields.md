---
description: 設定ICC配置檔案元資料欄位。
solution: Experience Manager
title: batchSetIccProfileFields
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: d10a30ca-afa7-4ef0-8cef-0329b0068bf3
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 14%

---

# batchSetIccProfileFields{#batchseticcprofilefields}

設定ICC配置檔案元資料欄位。

語法

## 授權的使用者類型 {#section-f6f7caf9434b4f469518dab64b76c0f4}

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
| `*`companyHandle`*` | `xsd:string` | 是 | 處理包含ICC配置檔案的公司。 |
| `*`更新陣列`*` | `xsd:string` | 是 | ICC配置檔案更新的陣列。 |

**輸出(batchSetIccProfileFields)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | 是 | 已成功設定ICC配置檔案欄位的數量。 |
| `*`warningCount`*` | `xsd:int` | 是 | 操作嘗試設定ICC配置檔案欄位時生成的警告數。 |
| `*`errorCount`*` | `xsd:int` | 是 | 嘗試設定ICC配置檔案欄位時生成的錯誤數。 |
| `*`warningDetailArray`*` | `types:AssetOperationFaultArray` | 否 | 與資產相關聯的詳細資訊陣列，當操作嘗試套用更新時，資產會產生警告。 |
| `*`errorDetailArray`*` | `types:AssetOperationFaultArray` | 否 | 與嘗試套用更新時產生錯誤之資產相關聯的詳細資訊陣列。 |

## 範例 {#section-5dc90cfbd9b1411485b44859032f7cb9}

**請求**

```java
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

**回答**

```java
<batchSetIccProfileFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</batchSetIccProfileFieldsReturn>
```
