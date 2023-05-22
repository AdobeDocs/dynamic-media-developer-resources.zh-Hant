---
description: 定義標籤欄位的搜索條件。
solution: Experience Manager
title: 標籤條件
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: ab1ac4b3-e91e-4c42-8b77-6e4c1d129b1a
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 7%

---

# [!DNL TagCondition]{#tagcondition}

定義標籤欄位的搜索條件。

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> 欄位句柄</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 標籤欄位句柄。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> op</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">取決於標籤欄位類型以及是否使用value或valueArray欄位。 
    <ul id="ul_CC0926425B094B3BB7D70CB392DBDABD">
     <li id="li_09AB923A9A8D4A71917CF59C150E4EF5">如果 <span class="codeph"> 值</span> 已通過， <span class="codeph"> 工作</span> 必須是字串常數匹配。 該條件與與標籤值關聯的任何資產匹配。 </li>
     <li id="li_70F18494AB6C454EB611F51F16C19FAD">如果 <span class="codeph"> 值陣列</span> 傳遞，op欄位可以是常數 <span class="codeph"> 匹配任意</span> 單值或多值標籤欄位。 A <span class="codeph"> 匹配任意</span> 條件匹配與中至少一個標籤值關聯的任何資產 <span class="codeph"> 值陣列</span>。 </li>
     <li id="li_0B25542D7E964B26B15591C45D5C66D0">對於多值標籤欄位，op欄位可設定為常數 <span class="codeph"> 全部匹配</span> 和 <span class="codeph"> 值陣列</span> 的子菜單。 在這種情況下，條件僅匹配與中所有標籤值關聯的資產 <span class="codeph"> 值陣列</span> （可能還有其他標籤值）。 </li>
    </ul></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 值</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 匹配值。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 值陣列</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：StringArray</span> </td> 
   <td colname="col3"> 多個匹配值。 </td> 
  </tr> 
 </tbody> 
</table>
