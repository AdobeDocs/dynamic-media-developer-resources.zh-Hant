---
description: 新增搜尋詞以搭配searchAssets使用。
seo-description: 新增搜尋詞以搭配searchAssets使用。
seo-title: 中繼資料條件
solution: Experience Manager
title: 中繼資料條件
topic: Scene7 Image Production System API
uuid: 9d65b8ce-86a5-4730-af84-a87134fd7db6
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 中繼資料條件{#metadatacondition}

新增搜尋詞以搭配searchAssets使用。

語法

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 名稱 </th> 
   <th colname="col2" class="entry"> 類型 </th> 
   <th colname="col3" class="entry"> 說明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 字 <span class="varname"> 段句柄</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 欄位控制代碼。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> op</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 字串比較運算子的選擇。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 值</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 測試值。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> boolVal</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 布林比較值（僅適用於布林類型欄位）。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 隆 <span class="varname"> 瓦爾</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:long</span> </td> 
   <td colname="col3"> 長比較值（僅適用於int-typed欄位）。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> minLong</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:long</span> </td> 
   <td colname="col3"> 範圍比較中的最小長值（僅適用於int-typed欄位）。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> maxLong</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:long</span> </td> 
   <td colname="col3"> 範圍比較中的最大長值（僅限int-typed欄位）。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> doubleVal</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:double</span> </td> 
   <td colname="col3"> 雙重比較值（僅適用於浮點型欄位）。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 最小雙</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:double</span> </td> 
   <td colname="col3"> 範圍比較中的最小雙重值（僅適用於浮動類型欄位）。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> maxDouble</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:double</span> </td> 
   <td colname="col3"> 範圍比較中的最大雙重值（僅適用於浮點類型欄位）。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> dateVale</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> 日期比較值（僅限日期類型欄位）。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 最 <span class="varname"> 小日期</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> 範圍比較中的最小日期值（僅限日期類型欄位）。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 最 <span class="varname"> 大日期</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> 範圍比較中的最大日期值（僅限日期類型欄位）。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 區 <span class="varname"> 分大小寫</span></span> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> <p> 建立中繼資料伺服器的區分大小寫功能。 用於searchAssetsByMetadata <span class="codeph"> 呼叫中</span> 。 </p> <p>請參 <a href="../../operations/c-operations-intro/c-methods/r-search-assets-by-metadata.md#reference-609ec73944a34ce49b152389fbb40414" format="dita" scope="local"> 閱searchAssetsByMetadata</a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

