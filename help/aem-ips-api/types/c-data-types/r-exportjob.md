---
description: 允許已授權匯出先前上傳檔案的工作型別。
solution: Experience Manager
title: ExportJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f0266b9f-c6e0-4843-b002-0bc068d43424
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 11%

---

# [!DNL ExportJob]{#exportjob}

允許已授權匯出先前上傳檔案的工作型別。

ExportJob不支援下列資產型別：

* 影像集
* 演算集
* 迴轉集
* 媒體集
* 多個位元速率設定
* 視訊集
* eCatalog
* 提案集

<table id="table_D8F3FD30D15648BFA5B980D3DC0A5AB1"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 名稱 </th> 
   <th colname="col2" class="entry"> 類型 </th> 
   <th colname="col3" class="entry"> 說明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> [!DNL assetHandleArray]</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph">型別：HandleArray</span> </p> </td> 
   <td colname="col3" valign="top"> <p>需要匯出的<span class="codeph">資產控制代碼</span>清單。 請參閱<a href="../../types/c-data-types/r-handle-array.md#reference-1b93fefb5477459faf9253b54349b5f9" type="reference" format="dita" scope="local"> HandleArray</a>。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> [!DNL fmt]</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd：字串</span> </p> </td> 
   <td colname="col3"> <p>指定<span class="codeph">匯出的型別。可能的值</span>： [orig， convert] </p> <p> 
     <ul id="ul_16EF4B14100C4C7AA464CA9CF7F11D1C"> 
      <li id="li_DAB2844CC55145C88A18A1F8EC4527F9">如果<span class="codeph"> fmt=orig</span>，資產會匯出為原始資產 </li> 
      <li id="li_07F2F8D159934D889FDC1022AB12B564">如果<span class="codeph"> fmt=convert</span>，資產會轉換為<span class="codeph"> is_modifer</span>或<span class="codeph">巨集</span>輸入引數中指定的格式 </li> 
     </ul> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> [!DNL is_modifier]</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd：字串</span> </p> </td> 
   <td colname="col3"> <p>指定附加至ExportJob <span class="codeph"> convert</span>請求的<span class="codeph"> ImageServer</span>轉譯URL字串。 </p> <p>如需傳送IS修飾元的詳細資訊，請參閱<a href="https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-serving-api/homeisir.html?lang=zh-Hant" scope="external" format="html"> IS檔案</a>。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> [!DNL macro]</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd：字串</span> </p> </td> 
   <td colname="col3"> <p></p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> [!DNL emailSetting]</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd：字串</span> </p> </td> 
   <td colname="col3"> <p>選擇電子郵件設定。 可能的值︰ </p> <p> 
     <ul id="ul_0EEDAE11B7CD4C53A6E4B2B8CB2CF730"> 
      <li id="li_F235F93828594ED78C6D464440F953FF"> <span class="codeph">全部</span> </li> 
      <li id="li_59E14E7EBFA64432A5FAC15DA21A0521"> <span class="codeph">錯誤</span> </li> 
      <li id="li_BFE0B52CADD14CC1BA1AF42AB0AA1CE1"> <span class="codeph"> ErrorAndWarning</span> </li> 
      <li id="li_BE3AA67E14FB487B8B9CD6EF3D58824C"> <span class="codeph">工作完成</span> </li> 
      <li id="li_409C68AD0D244975BFB86B08609E0146"> <span class="codeph">無</span> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> [!DNL clientId]</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd：字串</span> </p> </td> 
   <td colname="col3"> <p>指定起始匯出要求之使用者端或客戶的IP位址。 </p> <p> <p>備註：此引數目前並未主動填入，且嚴格保留僅供日後使用。 </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

對於已提供`fmt=convert`以及`is_modifier`和`macro`的ExportJob要求，目的地檔案會遵循`macro`所提供的格式。 例如: 

```
input_file = fileToExport.jpg
is_modifer = &fmt=png
macro=$test$ 
output_file = fileToExport.tiff
```
