---
description: 建立一般資產集，其原始集定義字串會發佈至影像伺服器。
solution: Experience Manager
title: createAssetSet
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '312'
ht-degree: 10%

---


# createAssetSet{#createassetset}

建立一般資產集，其原始集定義字串會發佈至影像伺服器。

語法

## 授權用戶類型{#section-d670d3af552147199b65c7eb847544a3}

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
   <td colname="col4"> 包含資產集之公司的控制代碼。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> folderHandle  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string  </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 將在其中建立新資產集的資料夾的句柄。 </td> 
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
   <td colname="col4"> 設定定義字串中的參數。 <p>這些必須解析為目標檢視器指定的格式。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> thumbAssetHandle  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string  </span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 當做新影像集縮圖的資產控制代碼。 如果未指定，IPS會嘗試使用該集所引用的第一個映像資產。 </td> 
  </tr> 
 </tbody> 
</table>

**setDefinition的替代函式**

您可以在目錄查閱或發佈期間解析的行中指定替代函式。 替代字串的格式為`${<substitution_func>}`。 下列列出可用的功能。

>[!NOTE]
>
>參數清單中的句柄文字必須用括弧`([])`括住。 在解析度期間，替代字串以外的所有文字都會逐字複製至輸出字串。

| **替代函式** | **退貨** |
|---|---|
| `getFilePath([asset_handle>])` | 資產的主要來源檔案路徑。 |
| `getCatalogId([<asset_handle>])` | 資產的目錄ID。 |
| `getMetaData([<asset_handle>], [<metadata_field_handle>])` | 資產的中繼資料值。 |
| `getThumbCatalogId([<asset_handle>])` | 資產的目錄ID（僅限影像型資產）。相關的拇指資產的目錄ID（適用於其他資產）。 如果關聯的縮圖資產不可用，函式會傳回空字串。 |

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

