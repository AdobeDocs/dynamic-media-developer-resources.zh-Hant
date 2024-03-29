---
description: 使用下列命令設定基本字元格式。
solution: Experience Manager
title: 基本字元格式設定
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d3bd6d4d-d7bd-4c9b-bc9e-7edaaac6378e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 7%

---

# 基本字元格式設定{#basic-character-formatting}

使用下列命令設定基本字元格式。

<table id="table_65415B84652F4E7497299AD90AE7C191"> 
 <thead> 
  <tr> 
   <th class="entry"> 命令 </th> 
   <th class="entry"> 說明 </th> 
   <th class="entry"> 附註 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <span class="codeph"> \一般 </span> </td> 
   <td> <p>將字元格式重設為預設值。 </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> 僅限。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \f <span class="varname"> N </span> </span> </td> 
   <td> <p>字型。 </p> </td> 
   <td> <p> <span class="codeph"> \fonttbl </span> 索引。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \fs <span class="varname"> N </span> </span> </td> 
   <td> <p>字型大小. </p> </td> 
   <td> <p>半點；預設為24。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \cf <span class="varname"> N </span> </span> </td> 
   <td> <p>字型色彩. </p> </td> 
   <td> <p>顏色資料表中以0為基礎的索引。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \b </span> </td> 
   <td> <p>粗體樣式。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \i </span> </td> 
   <td> <p>斜體樣式。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sub </span> </td> 
   <td> <p>下標。 </p> </td> 
   <td> <p>縮小字型大小。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \super </span> </td> 
   <td> <p>上標。 </p> </td> 
   <td> <p>縮小字型大小。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <span class="codeph"> \ul </span> </td> 
   <td> <p>加底線。 </p> </td> 
   <td> <p>「影像伺服」也會辨識下列RTF加底線指令： </p> <p> 
     <ul id="ul_EF2077DD51F94E2E94D8F1FA661F95DE"> 
      <li id="li_F9382148CCCC4A6AB373DD96D28B71EE"> <span class="codeph"> \uld </span> </li> 
      <li id="li_141276B2082E4AD0A8C7D3BDDADD6EE2"> <span class="codeph"> \uldash </span> </li> 
      <li id="li_32CE2C69EEFE462FB21F49FF52A65B0B"> <span class="codeph"> \uldashd </span> </li> 
      <li id="li_DCF3CD4F884845A5A6B84BDD8DB3A572"> <span class="codeph"> \uldashdd </span> </li> 
      <li id="li_FDEF96CCE14D41BDB878AADCFF73068F"> <span class="codeph"> \uldb </span> </li> 
      <li id="li_482CCC6F5D8544CCA69DF2A070097ABD"> <span class="codeph"> \ulth </span> </li> 
      <li id="li_F11C79A6640B4C0684CA5D9733E49F43"> <span class="codeph"> \ulw </span> </li> 
      <li id="li_84F94D17372B4C0494A9F8AEC951C556"> <span class="codeph"> \ulwave </span> </li> 
     </ul> </p> <p>目前這些是以標準形式實作 <span class="codeph"> \ul </span> 加底線。 所有其他RTF加底線指令都會被忽略。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ulnone </span> </td> 
   <td> <p>關閉底線 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ul0 </span> </td> 
   <td> <p>關閉底線 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \caps </span> </td> 
   <td> <p>大寫 </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> 僅限。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \scaps </span> </td> 
   <td> <p>小寫（「小型大寫字」） </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> 僅限。 </p> </td> 
  </tr> 
 </tbody> 
</table>
