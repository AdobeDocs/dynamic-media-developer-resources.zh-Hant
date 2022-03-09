---
description: 根據您指定的條件搜索資產。
solution: Experience Manager
title: 搜索資產
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 58bd80e4-e9eb-43e4-8508-04e330f0ad26
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '628'
ht-degree: 12%

---

# 搜索資產{#searchassets}

根據您指定的條件搜索資產。

語法

## searchAssets:關於 {#section-4ad74f12eb754768bf85bd235a7e25f0}

`searchAssets` 是檢索IPS資產的主要方法。 此方法用於各種目的，例如瀏覽資料夾層次結構或按名稱查找特定資產。

**響應大小**

`searchAssets` 在一次呼叫中返回多達1000個資產。 要每次呼叫返回最多10,000個資產，請將響應資料限制為 `totalRows`。 `name`。 `handle`。 `type`, `subType` 的子菜單。 要返回較大集，請使用 `resultPage` 的下界。

**使用responseFieldArray或excludeFieldArray限制結果檔案大小**

使用 `responseFieldArray` 或 `excludFieldArray` 參數。 這些參數有助於減少記憶體使用和頻寬，並可以縮短伺服器響應時間。

## 授權用戶類型 {#section-9c4bc41bb8b4493982197eb13c7cdc55}

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
>用戶必須具有讀取權限才能返回資產。

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> 公司句柄</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 包含要搜索的資產的公司的句柄。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> accessUserHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：字串</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 允許管理員以其他用戶的身份工作。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> accessGroupHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：字串</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 允許管理員作為不同組的一部分工作。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 資料夾</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：字串</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 用於搜索資產的根路徑。 如果省略，則使用公司根資料夾。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 包括子資料夾</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4">設定為 <span class="codeph"> 真</span> 搜索子資料夾。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 發佈狀態</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：字串</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 發佈狀態選擇。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 垃圾州</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：字串</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4">垃圾狀態選擇。 預設值為 <span class="codeph"> 不在垃圾</span>。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 條件匹配模式</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：字串</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p>搜索匹配模式的選擇 <span class="codeph"> 關鍵字陣列</span>。 </p> <p> <span class="codeph"> 條件匹配模式</span> </p> <p> <span class="codeph"> systemFieldConditionArray</span>, <span class="codeph"> 元資料條件陣列</span>。 預設值為 <span class="codeph"> 全部匹配</span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 關鍵字陣列</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：StringArray</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p> <p>注：已棄用的參數。 建議你別用它。 </p> </p> <p>要匹配的關鍵字字串陣列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 系統欄位匹配模式</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：字串</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p>組合搜索匹配模式的選擇 <span class="codeph"> 系統欄位條件</span> 匹配。 預設值為 <span class="codeph"> 全部匹配</span> </p>。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> systemFieldConditionArray</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 類型：SystemFieldConditionArray</span> </p> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 系統欄位條件的陣列。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 標籤匹配模式</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：字串</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4">搜索匹配模式字串常數。 預設值為 <span class="codeph"> 全部匹配</span>。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> tagConditionArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：TagConditionArray</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p>標籤欄位搜索謂詞的陣列。 </p> <p>謂語根據 <span class="codeph"> 標籤匹配模式</span> 設定，然後與任何術語組合 <span class="codeph"> 關鍵字陣列</span>。 <span class="codeph"> systemFieldConditionArray</span>, <span class="codeph"> 元資料條件陣列</span> 根據 <span class="codeph"> 條件匹配模式</span> 的子菜單。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 元資料匹配模式</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：字串</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4">搜索匹配模式以組合 <span class="codeph"> 元資料條件</span> 匹配。 預設值為 <span class="codeph"> 全部匹配</span>。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 元資料條件陣列</span> </span> </td> 
   <td colname="col2"> <p> <span class="codeph"> 類型：MetadataConditionArray</span> </p> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 元資料欄位搜索條件的陣列。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：StringArray</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 要包括在搜索中的資產類型陣列。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 排除AssetTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：StringArray</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 要從搜索中排除的資產類型陣列。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetSubTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：StringArray</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 要篩選的子類型名稱清單。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> strictSubTypeCheck</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：布爾</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4">如果 <span class="codeph"> 真</span> 和 <span class="codeph"> assetSubTypeArray</span> 不為空，只有子類型在的資產 <span class="codeph"> assetSubTypeArray</span> 的子菜單。 如果 <span class="codeph"> 假</span> （預設），則返回沒有定義子類型的資產。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 排除副產品</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：布爾</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 如果為true，則在接收主資產(如撕開的PDF頁影像)期間生成的副產品資產將從搜索結果中排除。 預設為 false。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 排除副產品陣列</span> </span> </td> 
   <td colname="col2"> <p> <span class="codeph"> 類型：排除副產品陣列</span> </p> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 要從搜索結果中排除的副產品資產生成條件陣列。 如果存在，則此參數將覆蓋excludeDisplusses設定。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 項目句柄</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sting</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 包含要搜索的資產的項目的處理。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 記錄每頁</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 要返回的最大結果數。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 結果頁</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4">根據 <span class="codeph"> 記錄每頁</span> 頁面大小。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 排序依據</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：字串</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 資產排序欄位的選擇。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 排序方向</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：字串</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 排序方向的選擇。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 響應欄位陣列</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：StringArray</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 包含要包含在響應中的欄位和子欄位的清單。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 排除欄位陣列</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：StringArray</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 包含要從響應中排除的欄位和子欄位的清單。 </td> 
  </tr> 
 </tbody> 
</table>

**輸出(searchAssetsReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 總行數 | `xsd:int` | 否 | 當每頁記錄不受限制時搜索返回的行數。 |
| 資產陣列 | `types:AssetArray` | 否 | 搜索返回的資產。 |

## 範例 {#section-725484cc09b54772a838ad2cc930b94b}

此代碼示例搜索屬於特定公司的映像資產。 響應被截斷以便簡化。

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
