---
description: 傳回Zip檔案資料。
solution: Experience Manager
title: getZipEntries
feature: Dynamic Media經典，SDK/API
role: 開發人員、管理員
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 20%

---


# getZipEntries{#getzipentries}

傳回Zip檔案資料。

語法

## 授權用戶類型{#section-33a3f03ba8a14086922397619ce12ab8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 參數 {#section-aa3f498fe76d4a5f99c42d64520fadce}

**輸入(getZipEntriesParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 包含Zip檔案之公司的控制代碼。 |
| `*`assetHandle`*` | `xsd:string` | 是 | Zip檔案的控制代碼。 |

**輸出(getZipEntriesReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`zipArray`*` | `types:ZipEntryArray` | 是 | Zip檔案中的項目陣列。 |

## 範例 {#section-1fc0ad8fa448492cb5a135d3e3d161ac}

此程式碼範例會傳回Zip檔案資訊，包括壓縮和解壓縮大小。

**請求**

```java
<getZipEntriesParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <assetHandle>a|94223|27|30602</assetHandle>
</getZipEntriesParam>
```

**回答**

```java
<getZipEntriesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <zipArray
      <items>
         <name>Checklist_Images/.DS_Store</name>
         <isDirectory>false</isDirectory>
         <lastModified>2007-05-09T15:41:52.000-07:00</lastModified>
         <compressedSize>503</compressedSize>
         <uncompressedSize>6148</uncompressedSize>
      </items>
   ...
   </zipArray>
</getZipEntriesReturn>
```

