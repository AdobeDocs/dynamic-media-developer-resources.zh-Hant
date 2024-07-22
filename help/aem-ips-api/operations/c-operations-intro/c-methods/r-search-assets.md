---
description: 根據您指定的條件搜尋資產。
solution: Experience Manager
title: 搜尋資產
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 58bd80e4-e9eb-43e4-8508-04e330f0ad26
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '630'
ht-degree: 6%

---

# 搜尋資產{#searchassets}

根據您指定的條件搜尋資產。

語法

## searchAssets：關於 {#section-4ad74f12eb754768bf85bd235a7e25f0}

`searchAssets`是擷取IPS資產的主要方法。 此方法可用於各種用途，例如瀏覽檔案夾階層或依名稱尋找特定資產。

**回應大小**

`searchAssets`在單一呼叫中最多可傳回1000個資產。 若要傳回每個呼叫最多10,000個資產，請將回應資料限製為`totalRows`、`name`、`handle`、`type`和`subType`欄位的子集。 若要傳回較大的集合，請使用`resultPage`引數設定分頁。

**使用responseFieldArray或excludeFieldArray限制結果檔案大小**

使用`responseFieldArray`或`excludFieldArray`引數限制資料集的大小。 這些引數有助於減少記憶體使用量和頻寬，並可改善伺服器回應時間。

## 授權的使用者型別 {#section-9c4bc41bb8b4493982197eb13c7cdc55}

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
>使用者必須擁有讀取存取權才能傳回資產。

## 參數 {#section-49aabc0600764f55a8b7017d86ded44f}

**輸入(searchAssetsParam)**

<table id="table_2972D1BB9CED4F7F9207747AE8CBAE8D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 名稱 </th> 
   <th colname="col2" class="entry"> 類型 </th> 
   <th colname="col3" class="entry"> 必填？ </th> 
   <th colname="col4" class="entry"> 說明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 擁有您要搜尋之資產的公司的控制代碼。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> accessUserHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 可讓管理員以其他使用者的身分工作。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> accessGroupHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 可讓管理員加入不同的群組。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname">資料夾</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 用於搜尋資產的根路徑。 如果省略，則使用公司根資料夾。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> includeSubfolders</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：布林值</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4">設定為<span class="codeph"> true</span>以搜尋子資料夾。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> publishState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> Publish州選擇。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> trashState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4">垃圾桶狀態選擇。 預設值為<span class="codeph"> NotInTrash</span>。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> conditionMatchMode</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p>選擇用於組合<span class="codeph"> keywordArray</span>結果的搜尋比對模式 </p> <p> <span class="codeph"> conditionMatchMode</span> </p> <p> <span class="codeph"> systemFieldConditionArray</span>和<span class="codeph"> metadataConditionArray</span>。 預設為<span class="codeph"> MatchAll</span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> keywordArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph">型別：StringArray</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p> <p>注意：已棄用的引數。 建議您不要使用它。 </p> </p> <p>要比對的關鍵字字字串陣列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> systemFieldMatchMode</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p>選擇搜尋比對模式以合併<span class="codeph">個systemFieldCondition</span>符合專案。 預設為<span class="codeph"> MatchAll</span> </p>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> systemFieldConditionArray</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph">型別：SystemFieldConditionArray</span> </p> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 系統欄位條件的陣列。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> tagMatchMode</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4">搜尋比對模式字串常數。 預設值為<span class="codeph"> MatchAll</span>。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> tagConditionArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph">型別：TagConditionArray</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p>標籤欄位搜尋述詞的陣列。 </p> <p>述詞是根據<span class="codeph"> tagMatchMode</span>設定進行組合，然後根據<span class="codeph"> conditionMatchMode</span>設定與<span class="codeph"> keywordArray</span>、<span class="codeph"> systemFieldConditionArray</span>和<span class="codeph"> metadataConditionArray</span>中的任何字詞進行組合。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> metadataMatchMode</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4">搜尋符合模式以合併<span class="codeph"> metadataCondition</span>個符合專案。 預設為<span class="codeph"> MatchAll</span>。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> metadataConditionArray</span> </span> </td> 
   <td colname="col2"> <p> <span class="codeph">型別：MetadataConditionArray</span> </p> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 中繼資料欄位搜尋條件的陣列。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph">型別：StringArray</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 要包含在搜尋中的資產型別陣列。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeAssetTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph">型別：StringArray</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 要從搜尋排除的資產型別陣列。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetSubTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph">型別：StringArray</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 要篩選的子型別名稱清單。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> strictSubTypeCheck</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：布林值</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4">如果<span class="codeph"> true</span>和<span class="codeph"> assetSubTypeArray</span>不是空的，則只會傳回子型別位於<span class="codeph"> assetSubTypeArray</span>中的資產。 如果<span class="codeph"> false</span> （預設），則會傳回未定義子型別的資產。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeByproducts</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：布林值</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 如果為True，則擷取主要資產期間產生的副產品資產(例如擷取的PDF頁面影像)會從搜尋結果中排除。 預設為 false。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludByproductArray</span> </span> </td> 
   <td colname="col2"> <p> <span class="codeph">型別：ExcludeByproductArray</span> </p> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 要從搜尋結果排除的副產品資產產生條件陣列。 如果存在，此引數會覆寫excludeByproducts設定。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname">專案控制代碼</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：sting</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 包含要搜尋之資產的專案控制代碼。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> recordsPerPage</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：int</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 要傳回的結果數上限。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname">個結果頁面</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：int</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4">根據<span class="codeph"> recordsPerPage</span>頁面大小，指定要傳回的結果頁面。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sortBy</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 選擇資產排序欄位。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sortDirection</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 選擇排序方向。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> responseFieldArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph">型別：StringArray</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 包含要包含在回應中的欄位和子欄位清單。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeFieldArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph">型別：StringArray</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 包含從回應中排除的欄位和子欄位清單。 </td> 
  </tr> 
 </tbody> 
</table>

**輸出(searchAssetsReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| totalRows | `xsd:int` | 否 | 每頁的記錄數不受限制時，搜尋傳回的列數。 |
| assetArray | `types:AssetArray` | 否 | 搜尋傳回的Assets。 |

## 範例 {#section-725484cc09b54772a838ad2cc930b94b}

此程式碼範例會搜尋屬於特定公司的影像資產。 為簡短起見，回應會遭截斷。

**要求**

```java
<ns1:searchAssetsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:includeSubfolders>true</ns1:includeSubfolders>
   <ns1:assetTypeArray>
      <ns1:items>Image</ns1:items>
   </ns1:assetTypeArray>
</ns1:searchAssetsParam>
```

**回應**

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
