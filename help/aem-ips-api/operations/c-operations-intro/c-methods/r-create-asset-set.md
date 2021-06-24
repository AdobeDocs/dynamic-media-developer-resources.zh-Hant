---
description: 建立一般資產集，其中包含要發佈至影像伺服器的原始集定義字串。
solution: Experience Manager
title: createAssetSet
feature: Dynamic Media Classic,SDK/API，資產管理
role: Developer,Administrator
exl-id: 4565eb4f-eeb7-4b98-bfef-1a59e9a931af
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 10%

---

# createAssetSet{#createassetset}

建立一般資產集，其中包含要發佈至影像伺服器的原始集定義字串。

語法

## 授權的使用者類型 {#section-d670d3af552147199b65c7eb847544a3}

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 將包含資產集之公司的控制代碼。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> folderHandle  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string  </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 將在其中建立新資產集的資料夾的控制代碼。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 名稱  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string  </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 資產名稱。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> subType  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string  </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 由用戶端為資產集類型建立的唯一識別碼。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> setDefinition  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string  </span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 設定定義字串中的參數。 <p>這些參數必須解析為目標檢視器指定的格式。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> thumbAssetHandle  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string  </span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 作為新影像集縮圖的資產處理。 如果未指定，IPS會嘗試使用由集引用的第一個影像資產。 </td> 
  </tr> 
 </tbody> 
</table>

**setDefinition的替代函式**

您可以在目錄查找或發佈期間解析的行中指定替代函式。 替代字串的格式為`${<substitution_func>}`。 下面列舉了可用的功能。

>[!NOTE]
>
>參數清單中的句柄文字必須由括弧`([])`包圍。 在解析期間，替代字串之外的所有文本將逐字複製到輸出字串。

| **替代函式** | **傳回** |
|---|---|
| `getFilePath([asset_handle>])` | 資產的主要來源檔案路徑。 |
| `getCatalogId([<asset_handle>])` | 資產的目錄ID。 |
| `getMetaData([<asset_handle>], [<metadata_field_handle>])` | 資產的中繼資料值。 |
| `getThumbCatalogId([<asset_handle>])` | 資產的目錄ID（僅適用於影像型資產）。關聯的縮圖資產的目錄ID（適用於其他資產）。 如果相關聯的縮圖資產無法使用，函式會傳回空白字串。 |

**範例媒體setDefinition字串**

```java
${getCatalogId([a|1664|22|1664])};${getCatalogId([a|1664|22|1664])};1,${getFilePath([a|103 
6|19|144])};${getCatalogId([a|452|1|433])};2;${getMetadata([a|1036|19|144], [m|1|ASSET|SharedDateField])} 
```

在目錄查閱或發佈時，這會解析為類似下列的字串：

```java
jcompany/myRenderSet;jcompany/myRenderSet;1,jcompany/Videos/Somebodys_N08275_flv.flv;jcomp any/myimg-1;2;20090703 10:05:53
```

**輸出(createAssetSet)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`assetHandle`*` | `xsd:string` | 是 | 資產集的控制代碼。 |

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
