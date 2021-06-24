---
description: 定義標籤欄位的搜尋條件。
solution: Experience Manager
title: TagCondition
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: ab1ac4b3-e91e-4c42-8b77-6e4c1d129b1a
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 7%

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 標籤欄位句柄。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> op</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">取決於標籤欄位類型，以及是否使用值或valueArray欄位。 
    <ul id="ul_CC0926425B094B3BB7D70CB392DBDABD">
     <li id="li_09AB923A9A8D4A71917CF59C150E4EF5">如果傳遞了<span class="codeph">值</span>,<span class="codeph"> op</span>必須是字串常數「符合」。 條件符合與標籤值相關聯的任何資產。 </li>
     <li id="li_70F18494AB6C454EB611F51F16C19FAD">如果傳遞了<span class="codeph"> valueArray</span>，則op欄位可以是單值或多值標籤欄位的常數<span class="codeph"> MatchesAny</span>。 <span class="codeph">符合Any</span>條件符合與<span class="codeph"> valueArray</span>中至少一個標籤值相關聯的任何資產。 </li>
     <li id="li_0B25542D7E964B26B15591C45D5C66D0">對於多值標籤欄位，op欄位可設為常數<span class="codeph">與<span class="codeph"> valueArray</span>欄位相符的MatchesAll</span> 。 在此情況下，條件僅符合與<span class="codeph"> valueArray</span>中所有標籤值（可能還有其他標籤值）相關聯的資產。 </li>
    </ul></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> value</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 相符的值。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> valueArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：StringArray</span> </td> 
   <td colname="col3"> 多個相符值。 </td> 
  </tr> 
 </tbody> 
</table>
