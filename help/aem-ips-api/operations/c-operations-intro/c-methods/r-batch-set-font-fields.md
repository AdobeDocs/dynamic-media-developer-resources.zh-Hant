---
description: 設定字型元資料欄位。
solution: Experience Manager
title: batchSetFontFields
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f38aa861-2a81-4663-967e-72611122f51b
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 15%

---

# batchSetFontFields{#batchsetfontfields}

設定字型元資料欄位。

## 授權用戶類型 {#section-89eff13b5ed54cddb87b1304ba4eff0e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 參數 {#section-836f5948d00a46e98ccb62f0573e4e68}

**Input(batchSetFontFieldsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 公司句柄 | `xsd:string` | 是 | 對包含字型的公司進行句柄。 |
| 更新陣列 | `types:FontFieldUpdateArray` | 是 | 字型欄位更新的陣列。 |

**輸出(batchSetFontFieldsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 成功計數 | `xsd:int` | 是 | 成功設定字型欄位的數目。 |
| 警告計數 | `xsd:int` | 是 | 嘗試設定字型欄位時生成的警告數。 |
| 錯誤計數 | `xsd:int` | 是 | 嘗試設定字型欄位時生成的錯誤數。 |
| 警告DetailArray | `types:AssetOperationFaultArray` | 否 | 與在操作嘗試應用更新時生成警告的資產關聯的詳細資訊陣列。 |
| 錯誤DetailArray | `types:AssetOperationFaultArray` | 否 | 與在操作嘗試應用更新時生成錯誤的資產關聯的詳細資訊陣列。 |

## 範例 {#section-0449c2e4ec534f4b8ee849ec4fe12c4e}

**請求**

```javascript {.line-numbers}
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

```javascript {.line-numbers}
<batchSetFontFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</batchSetFontFieldsReturn>
```
