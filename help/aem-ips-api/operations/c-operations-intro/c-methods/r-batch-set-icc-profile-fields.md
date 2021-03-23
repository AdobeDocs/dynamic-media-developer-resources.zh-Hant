---
description: 設定ICC配置檔案元資料欄位。
seo-description: 設定ICC配置檔案元資料欄位。
seo-title: batchSetIccProfileFields
solution: Experience Manager
title: batchSetIccProfileFields
uuid: 163b9b36-85b6-4880-8029-8421b04f4a08
feature: Dynamic Media經典，SDK/API
role: 開發人員、管理員
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 13%

---


# batchSetIccProfileFields{#batchseticcprofilefields}

設定ICC配置檔案元資料欄位。

語法

## 授權用戶類型{#section-f6f7caf9434b4f469518dab64b76c0f4}

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
| `*`companyHandle`*` | `xsd:string` | 是 | 包含ICC設定檔的公司控制代碼。 |
| `*`更新陣列`*` | `xsd:string` | 是 | ICC設定檔更新陣列。 |

**輸出(batchSetIccProfileFields)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | 是 | 成功設定ICC配置檔案欄位的數量。 |
| `*`warningCount`*` | `xsd:int` | 是 | 嘗試設定ICC配置檔案欄位時生成的警告數。 |
| `*`errorCount`*` | `xsd:int` | 是 | 嘗試設定ICC配置檔案欄位時生成的錯誤數。 |
| `*`warningDetailArray`*` | `types:AssetOperationFaultArray` | 否 | 與資產相關的詳細資訊陣列，當操作嘗試套用更新時，這些資產會產生警告。 |
| `*`errorDetailArray`*` | `types:AssetOperationFaultArray` | 否 | 當操作嘗試套用更新時，與產生錯誤的資產相關的詳細資訊陣列。 |

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

