---
description: 為與setAssetMetadata一起使用的特定資產設定元資料值。 描述要對元資料所做的更改。
solution: Experience Manager
title: 元資料更新
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: 99dc1f0c-c4c4-433e-9b91-fa39ef6f84d7
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 4%

---

# 元資料更新{#metadataupdate}

為與setAssetMetadata一起使用的特定資產設定元資料值。 描述要對元資料所做的更改。

>[!NOTE]
>
>如果傳遞了單值欄位，則資產的標籤值將重置為指定的標籤值。

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> 欄位句柄</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 元資料欄位句柄。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 值</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：字串</span> </td> 
   <td colname="col3"> 元資料更新值。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 布爾瓦爾</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 布爾元資料值（僅適用於布爾類型欄位）。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 朗瓦爾</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:long</span> </td> 
   <td colname="col3"> 長元資料值（僅適用於int類型欄位）。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 雙谷</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：雙</span> </td> 
   <td colname="col3"> 雙元資料值（僅適用於浮點類型欄位）。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 日期值</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> 日期元資料值（僅適用於日期類型欄位）。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> addTagValueArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：StringArray</span> </td> 
   <td colname="col3"> <p>添加到資產的現有標籤值清單。 
     <ul id="ul_08DE6C490B614560A6118E7AC59720E3"> 
      <li id="li_358A3BDC0EC94CCF8178CD789F09F804">單值標籤欄位僅儲存最後一個值。 </li> 
      <li id="li_3F47D3A3C63A4752BF9A45F7B00A6E70">如果值不在字典中，則固定字典標籤欄位返回錯誤。 </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> setTagValueArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：StringArray</span> </td> 
   <td colname="col3">替換資產的現有標籤值清單。 
    <ul id="ul_941C915C69E84CF2AC5938378837EB92"> 
     <li id="li_6E85019335034B2EB1302696AE690ED5">單值標籤欄位僅儲存最後一個值。 </li> 
     <li id="li_0DC56717EBB642D29FB7A3D043CEDED1">如果值不在字典中，則固定字典標籤欄位返回錯誤。 </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> deleteTagValueArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：StringArray</span> </td> 
   <td colname="col3"> 從資產的標籤值清單中刪除指定的值（如果存在）。 </td> 
  </tr> 
 </tbody> 
</table>
