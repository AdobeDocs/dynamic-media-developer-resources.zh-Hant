---
description: 定義標籤欄位的搜尋條件。
solution: Experience Manager
title: TagCondition
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: ab1ac4b3-e91e-4c42-8b77-6e4c1d129b1a
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 3%

---

# [!DNL TagCondition]{#tagcondition}

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
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> 標籤欄位控制代碼。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname">作業</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3">取決於標籤欄位型別以及使用的是value還是valueArray欄位。 
    <ul id="ul_CC0926425B094B3BB7D70CB392DBDABD">
     <li id="li_09AB923A9A8D4A71917CF59C150E4EF5">如果傳遞<span class="codeph">值</span>，則<span class="codeph">op</span>必須是字串常數符合。 條件符合與標籤值相關聯的任何資產。 </li>
     <li id="li_70F18494AB6C454EB611F51F16C19FAD">如果傳遞<span class="codeph"> valueArray</span>，則單值或多值標籤欄位的作業欄位可以是常數<span class="codeph"> MatchesAny</span>。 <span class="codeph"> MatchesAny</span>條件符合<span class="codeph"> valueArray</span>中至少一個標籤值關聯的任何資產。 </li>
     <li id="li_0B25542D7E964B26B15591C45D5C66D0">對於多值標籤欄位，操作欄位可以設定為包含<span class="codeph"> valueArray</span>欄位的常數<span class="codeph"> MatchesAll</span>。 在此情況下，條件只會符合與<span class="codeph"> valueArray</span>中所有標籤值相關聯的資產（可能還有其他標籤值之外）。 </li>
    </ul></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname">值</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> 相符的值。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> valueArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph">型別：StringArray</span> </td> 
   <td colname="col3"> 多個相符的值。 </td> 
  </tr> 
 </tbody> 
</table>
