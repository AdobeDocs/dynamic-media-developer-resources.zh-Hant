---
description: 更新現有資產集的集定義。
solution: Experience Manager
title: setAssetSetDefinition
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: f3fbe13b-e650-4a5d-9c46-a492b11fa13e
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 6%

---

# setAssetSetDefinition{#setassetsetdefinition}

更新現有資產集的集定義。

語法

## 授權用戶類型 {#section-9d4ca3a8cfe74934b89971de01a2143c}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 參數 {#section-c2057a5a13d042c684a3da1b49bc5dc6}

**Input(setAssetDefinitionParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 公司句柄 | `xsd:string` | 是 | 具有資產集的公司的句柄。 |
| 資產句柄 | `xsd:string` | 是 | 資產集句柄 |
| setDefinition | `xsd:string` | 是 | 定義字串。 參見下面。 |

**輸出(setAssetSetDefinitionReturn)**

IPS API不會為此操作返迴響應。

## setDefinition參數：關於 {#section-f88e066bf5294b4f8c12d5d652a5c94c}

**setDefinition函式**

指定 `setDefinition` 替代函式串聯。 在目錄查找或發佈時解決這些問題。 替代字串的格式 `${<substitution_func>}`，並包括以下內容：

>[!NOTE]
>
>參數清單中的處理文字必須用括弧括起來 `([])`。 在解析期間，替換字串外的文本將複製到輸出字串。

<table id="table_A93D2C273B694C289208AA926B2597CD"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 替代函式 </th> 
   <th colname="col2" class="entry"> 返回資產 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> getFilePath([ <span class="varname"> asset_handle </span>]) </span> </td> 
   <td colname="col2"> 主檔案路徑。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> getCatalogd([ <span class="varname"> asset_handle </span>]) </span> </td> 
   <td colname="col2"> 目錄ID。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> getMetaData([ <span class="varname"> asset_handle </span>],[ <span class="varname"> 元資料_欄位_句柄 </span>]) </span> </td> 
   <td colname="col2"> 元資料值。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> getThumbCatalogId([ <span class="varname"> asset_handle </span>]) </span> </td> 
   <td colname="col2"> 目錄ID。 應用於基於影像的資產（影像、調整後的視圖、圖層視圖）。 <p>對於其他資產，返回拇指資產的目錄ID（如果有）。 如果沒有拇指資產與資產關聯，則函式返回空字串。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**setDefinition示例**

此媒體集定義字串：

```java
${getCatalogId([a|1664|22|1664])};${getCatalogId([a|1664|22|1664])}; 
1,${getFilePath([a|1036|19|144])};${getCatalogId([a|452|1|433])};2; 
${getMetadata([a|1036|19|144], [m|1|ASSET|SharedDateField])}
```

在查找或發佈時解析為以下內容：

```java
jcompany/myRenderSet;jcompany/myRenderSet; 
1,jcompany/Videos/N08275_flv.flv;jcompany/myimg-1;2;20090703 10:05:53
```

## 範例 {#section-739b42eec3074cafae285ec015a2d088}

**請求**

```java
<setAssetSetDefinitionParam xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31"> 
   <companyHandle>c|1</companyHandle> 
   <assetHandle>a|1802|44|1802</assetHandle> 
   <setDefinition>${getCatalogId([a|1553|1|1176])};${getCatalogId([a|1553|1|1176])};1;img1, 
   ${getCatalogId([a|632|1|452])};${getCatalogId([a|632|1|452])};1,${getCatalogId([a|1664|22|1664])}; 
   ${getCatalogId([a|1664|22|1664])};1,${getFilePath([a|1036|19|144])};${getCatalogId([ a|452|1|433])}; 
   2;${getMetadata([a1036|19|144], [m|1|ASSET|SharedDateField])}</setDefinition> 
</setAssetSetDefinitionParam>
```

**回答**

無。
