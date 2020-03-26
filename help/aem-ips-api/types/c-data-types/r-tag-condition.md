---
description: 定義標籤欄位的搜尋條件。
seo-description: 定義標籤欄位的搜尋條件。
seo-title: TagCondition
solution: Experience Manager
title: TagCondition
topic: Scene7 Image Production System API
uuid: c7727267-05b6-4011-9ddf-7f3134e9609b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# TagCondition{#tagcondition}

定義標籤欄位的搜尋條件。

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
   <td colname="col3"> 標籤欄位控制代碼。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> op</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">視標籤欄位類型以及是否使用value或valueArray欄位而定。 
    <ul id="ul_CC0926425B094B3BB7D70CB392DBDABD">
     <li id="li_09AB923A9A8D4A71917CF59C150E4EF5">如果 <span class="codeph"> 傳遞值</span> , <span class="codeph"> op</span> 必須是字串常數Matches。 條件符合與標籤值相關聯的任何資產。 </li>
     <li id="li_70F18494AB6C454EB611F51F16C19FAD">如果 <span class="codeph"> 傳遞valueArray</span> ,op欄位可以是單值或多值標籤欄位 <span class="codeph"> 的常數MatchesAny</span> 。 MatchesAny <span class="codeph"> 條件</span> ，會比對與valueArray中至少一個標籤值相關聯的任何資 <span class="codeph"> 產</span>。 </li>
     <li id="li_0B25542D7E964B26B15591C45D5C66D0">對於多值標籤欄位，op欄位可以設定為常數MatchesAll <span class="codeph"> with</span> valueArray欄位 <span class="codeph"></span> 。 在這種情況下，條件僅匹配與valueArray中所有標籤值（可能還有其他標籤值）相關聯的 <span class="codeph"> 資產</span> 。 </li>
    </ul></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 值</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 相符值。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> valueArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：StringArray</span> </td> 
   <td colname="col3"> 多個相符值。 </td> 
  </tr> 
 </tbody> 
</table>

