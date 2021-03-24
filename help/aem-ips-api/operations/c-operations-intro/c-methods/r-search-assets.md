---
description: 根據您指定的條件搜尋資產。
solution: Experience Manager
title: searchAssets
feature: Dynamic Media經典，SDK/API，資產管理
role: 開發人員、管理員
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '637'
ht-degree: 12%

---


# searchAssets{#searchassets}

根據您指定的條件搜尋資產。

語法

## searchAssets:關於{#section-4ad74f12eb754768bf85bd235a7e25f0}

`searchAssets` 是檢索IPS資產的主要方法。此方法用於各種用途，例如瀏覽資料夾階層或依名稱尋找特定資產。

**回應大小**

`searchAssets` 在單一呼叫中傳回最多1000個資產。若要每次呼叫傳回最多10,000個資產，請將回應資料限制在`totalRows`、`name`、`handle`、`type`和`subType`欄位的子集。 若要傳回較大的集，請使用`resultPage`參數設定分頁。

**使用responseFieldArray或excludeFieldArray限制結果檔案大小**

使用`responseFieldArray`或`excludFieldArray`參數限制資料集的大小。 這些參數有助於減少記憶體使用和頻寬，並可改善伺服器回應時間。

## 授權用戶類型{#section-9c4bc41bb8b4493982197eb13c7cdc55}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>使用者必須擁有傳回資產的讀取存取權。

## 參數 {#section-49aabc0600764f55a8b7017d86ded44f}

**輸入(searchAssetsParam)**

<table id="table_2972D1BB9CED4F7F9207747AE8CBAE8D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 名稱 </th> 
   <th colname="col2" class="entry"> 類型 </th> 
   <th colname="col3" class="entry"> 必要? </th> 
   <th colname="col4" class="entry"> 說明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 包含您要搜尋之資產之公司的控制代碼。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> accessUserHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 可讓管理員以不同的使用者身分工作。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> accessGroupHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 可讓管理員以不同群組的一部分工作。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 資料夾</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 用於搜尋資產的根路徑。 若省略，則會使用公司根資料夾。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> includeSubfolders</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4">設為<span class="codeph"> true</span>可搜尋子檔案夾。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> publishState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 發佈狀態選擇。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> trashState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4">垃圾狀態選擇。 預設值為<span class="codeph"> NotInTrash</span>。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> conditionMatchMode</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p>選擇搜尋符合模式，以結合<span class="codeph"> keywordArray</span>的結果， </p> <p> <span class="codeph"> conditionMatchMode</span> </p> <p> <span class="codeph"> systemFieldConditionArray</span>和metadataConditionArray <span class="codeph"> </span>。預設值為<span class="codeph"> MatchAll</span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> keywordArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：StringArray</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p> <p>注意： 不建議使用的參數。 建議您不要使用它。 </p> </p> <p>要比對的關鍵字字串陣列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> systemFieldMatchMode</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p>組合<span class="codeph"> systemFieldCondition</span>的搜尋符合模式選擇。 預設值為<span class="codeph"> MatchAll</span> </p>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> systemFieldConditionArray</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 類型：SystemFieldConditionArray</span> </p> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 系統欄位條件的陣列。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> tagMatchMode</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4">搜尋符合模式字串常數。 預設值為<span class="codeph"> MatchAll</span>。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> tagConditionArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：TagConditionArray</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p>標籤欄位搜索謂語的陣列。 </p> <p>謂語根據<span class="codeph"> tagMatchMode</span>設定組合，然後根據<span class="codeph">條件與<span class="codeph"> keywordArray</span>、<span class="codeph"> systemFieldConditionArray</span>和<span class="codeph"> metadataConditionArray</span>中的任何詞語組合模式</span>設定。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> metadataMatchMode</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4">搜尋符合模式以組合<span class="codeph"> metadataCondition</span>符合。 預設值為<span class="codeph"> MatchAll</span>。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> metadataConditionArray</span> </span> </td> 
   <td colname="col2"> <p> <span class="codeph"> 類型：MetadataConditionArray</span> </p> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 中繼資料欄位搜尋條件的陣列。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：StringArray</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 要納入搜尋的資產類型陣列。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeAssetTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：StringArray</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 要從搜尋中排除的資產類型陣列。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetSubTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：StringArray</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 要篩選的子類型名稱清單。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> strictSubTypeCheck</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：布林值</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4">如果<span class="codeph"> true</span>和<span class="codeph"> assetSubTypeArray</span>並非空白，則只會傳回子類型位於<span class="codeph"> assetSubTypeArray</span>中的資產。 如果<span class="codeph"> false</span>（預設值），則會傳回未定義子類型的資產。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeBilluss</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：布林值</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 如果為true，則擷取主要資產（例如擷取的PDF頁面影像）時產生的副產品資產會排除在搜尋結果之外。 預設為 false。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludBinsubleArray</span> </span> </td> 
   <td colname="col2"> <p> <span class="codeph"> 類型：ExcludeBinsulalArray</span> </p> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 要從搜尋結果中排除的副產品資產產生條件的陣列。 如果存在，此參數將覆蓋excludeBillussings設定。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> projectHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sting</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 包含要搜尋之資產的專案處理。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> recordsPerPage</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 要傳回的最大結果數。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> resultsPage</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4">根據<span class="codeph"> recordsPerPage</span>頁面大小，指定要傳回的結果頁面。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sortBy</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 資產排序欄位的選項。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sortDirection</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 排序方向的選擇。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> responseFieldArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：StringArray</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 包含要包含在回應中的欄位和子欄位清單。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeFieldArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：StringArray</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 包含要從回應中排除的欄位和子欄位清單。 </td> 
  </tr> 
 </tbody> 
</table>

**輸出(searchAssetsReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`totalRows`*` | `xsd:int` | 否 | 當每頁記錄不受限制時，搜尋傳回的列數。 |
| `*`assetArray`*` | `types:AssetArray` | 否 | 搜尋傳回的資產。 |

## 範例 {#section-725484cc09b54772a838ad2cc930b94b}

此程式碼範例會搜尋屬於特定公司的影像資產。 回應會因簡短而截斷。

**請求**

```java
<ns1:searchAssetsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:includeSubfolders>true</ns1:includeSubfolders>
   <ns1:assetTypeArray>
      <ns1:items>Image</ns1:items>
   </ns1:assetTypeArray>
</ns1:searchAssetsParam>
```

**回答**

```java
<searchAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <totalRows>210</totalRows>
   <assetArray>
      <items>
         <assetHandle>24265|1|17061</assetHandle>
         <type>Image</type>
         <name>Autumn Leaves</name>
         ...
      </items>
    </assetArray>
</searchAssetsReturn>
```

