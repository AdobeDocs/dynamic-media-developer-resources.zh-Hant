---
description: 設定字型元資料欄位。
solution: Experience Manager
title: batchSetFontFields
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: f38aa861-2a81-4663-967e-72611122f51b
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 14%

---

# batchSetFontFields{#batchsetfontfields}

設定字型元資料欄位。

## 授權的使用者類型 {#section-89eff13b5ed54cddb87b1304ba4eff0e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 參數 {#section-836f5948d00a46e98ccb62f0573e4e68}

**輸入(batchSetFontFieldsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 對包含字型的公司進行處理。 |
| `*`updateArray`*` | `types:FontFieldUpdateArray` | 是 | 字型欄位更新的陣列。 |

**輸出(batchSetFontFieldsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | 是 | 已成功設定字型欄位的數目。 |
| `*`warningCount`*` | `xsd:int` | 是 | 嘗試設定字型欄位時生成的警告數。 |
| `*`errorCount`*` | `xsd:int` | 是 | 嘗試設定字型欄位時生成的錯誤數。 |
| `*`warningDetailArray`*` | `types:AssetOperationFaultArray` | 否 | 與資產相關聯的詳細資訊陣列，當操作嘗試套用更新時，資產會產生警告。 |
| `*`errorDetailArray`*` | `types:AssetOperationFaultArray` | 否 | 與嘗試套用更新時產生錯誤之資產相關聯的詳細資訊陣列。 |

## 範例 {#section-0449c2e4ec534f4b8ee849ec4fe12c4e}

**請求**

```java
<batchSetFontFieldsParam xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <companyHandle>c|1</companyHandle>
   <updateArray>
      <items>
          <assetHandle>a|450|14|19</assetHandle>
          <fontName>Bookman Old Style Font Name</fontName>
          <postscriptName>Bookman Old Style PostScript</postscriptName>
          <rtfName>Bookman Old Style RTF</rtfName>
          <fontFamily>Bookman Old Style Family</fontFamily>
          <style>BoldItalic</style>
          <typeName>Open Type</typeName><type>OTF</type>
      </items>
   </updateArray>
</batchSetFontFieldsParam>
```

**回答**

```java
<batchSetFontFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</batchSetFontFieldsReturn>
```
