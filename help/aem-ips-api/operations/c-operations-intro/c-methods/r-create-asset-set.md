---
description: 使用原始集定義字串建立要發佈到映像伺服器的常規資產集。
solution: Experience Manager
title: createAssetSet
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 4565eb4f-eeb7-4b98-bfef-1a59e9a931af
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 10%

---

# createAssetSet{#createassetset}

使用原始集定義字串建立要發佈到映像伺服器的常規資產集。

語法

## 授權用戶類型 {#section-d670d3af552147199b65c7eb847544a3}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 參數 {#section-3580b586296e42a5b21426085b1bb72d}

**輸入(createAssetSet)**

<table id="table_2C70C33A127242FC828FCD8EC852E1EC"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 名稱 </th> 
   <th colname="col2" class="entry"> 類型 </th> 
   <th colname="col3" class="entry"> 必要 </th> 
   <th colname="col4" class="entry"> 說明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 公司句柄 </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 包含資產集的公司的句柄。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> folderHandle </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：字串 </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 建立新資產集的資料夾的句柄。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 名稱 </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：字串 </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 資產名稱。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 子類型 </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：字串 </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 客戶端為資產集類型建立的唯一標識符。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> setDefinition </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：字串 </span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 集定義字串中的參數。 <p>必須解析為目標查看器指定的格式。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 拇指資產句柄 </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：字串 </span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 用作新影像集縮略圖的資產的句柄。 如果未指定，IPS將嘗試使用該集引用的第一個影像資源。 </td> 
  </tr> 
 </tbody> 
</table>

**setDefinition的替代函式**

您可以在目錄查找或發佈期間解析的行中指定替代函式。 替代字串的格式 `${<substitution_func>}`。 下面列舉了可用的函式。

>[!NOTE]
>
>參數清單中的句柄文字必須用括弧括起來 `([])`。 在解析期間，替換字串之外的所有文本將逐字複製到輸出字串。

| **替代函式** | **返回** |
|---|---|
| `getFilePath([asset_handle>])` | 資產的主源檔案路徑。 |
| `getCatalogId([<asset_handle>])` | 資產的目錄ID。 |
| `getMetaData([<asset_handle>], [<metadata_field_handle>])` | 資產的元資料值。 |
| `getThumbCatalogId([<asset_handle>])` | 資產的目錄ID（僅適用於基於映像的資產）。關聯的拇指資產的目錄ID（適用於其他資產）。 如果關聯的拇指資產不可用，則函式返回空字串。 |

**媒體集定義字串示例**

```java
${getCatalogId([a|1664|22|1664])};${getCatalogId([a|1664|22|1664])};1,${getFilePath([a|103 
6|19|144])};${getCatalogId([a|452|1|433])};2;${getMetadata([a|1036|19|144], [m|1|ASSET|SharedDateField])} 
```

在目錄查找或發佈時，將解析為類似於以下內容的字串：

```java
jcompany/myRenderSet;jcompany/myRenderSet;1,jcompany/Videos/Somebodys_N08275_flv.flv;jcomp any/myimg-1;2;20090703 10:05:53
```

**輸出(createAssetSet)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 資產句柄 | `xsd:string` | 是 | 資產集的句柄。 |

## 範例 {#section-fed53089de824d67ab96cd9103d384b4}

**請求**

```java
<createAssetSetParam xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31"> 
   <companyHandle>c|1</companyHandle> 
   <folderHandle>f|jcompany/AssetSets/</folderHandle> 
   <name>testAssetSet</name> 
   <subType>MediaSet</subType> 
</createAssetSetParam>
```

**回答**

```java
<createAssetSetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31"> 
   <assetHandle>a|1801|44|1801</assetHandle> 
</createAssetSetReturn>
```
