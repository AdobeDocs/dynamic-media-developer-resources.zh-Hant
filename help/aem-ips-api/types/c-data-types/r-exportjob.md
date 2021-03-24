---
description: 作業類型，允許授權匯出先前上傳的檔案。
solution: Experience Manager
title: ExportJob
feature: Dynamic Media經典，SDK/API
role: 開發人員、管理員
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 16%

---


# ExportJob{#exportjob}

作業類型，允許授權匯出先前上傳的檔案。

ExportJob不支援下列資產類型：

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
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> assetHandleArray</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 類型：HandleArray</span> </p> </td> 
   <td colname="col3" valign="top"> <p>需要導出的<span class="codeph"> assetHandle</span>的清單。 請參閱<a href="../../types/c-data-types/r-handle-array.md#reference-1b93fefb5477459faf9253b54349b5f9" type="reference" format="dita" scope="local"> HandleArray</a>。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> fmt</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string </span> </p> </td> 
   <td colname="col3"> <p>指定<span class="codeph"> export.Possible Values</span>的類型：[orig, convert] </p> <p> 
     <ul id="ul_16EF4B14100C4C7AA464CA9CF7F11D1C"> 
      <li id="li_DAB2844CC55145C88A18A1F8EC4527F9">如果<span class="codeph"> fmt=orig</span>，則將資產導出為原始資產 </li> 
      <li id="li_07F2F8D159934D889FDC1022AB12B564">如果<span class="codeph"> fmt=convert</span>，則將資產轉換為在<span class="codeph"> is_modifer</span>或<span class="codeph">宏</span>輸入參數中指定的格式 </li> 
     </ul> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> is_modifier</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string  </span> </p> </td> 
   <td colname="col3"> <p>指定<span class="codeph"> ImageServer</span>轉換URL字串，該字串會附加至ExportJob <span class="codeph"> convert</span>請求。 </p> <p>有關發送IS修飾詞的詳細資訊，請參閱<a href="https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-serving-api/home.html" scope="external" format="html"> IS文檔</a>。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 宏</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string  </span> </p> </td> 
   <td colname="col3"> <p></p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> emailSetting</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string  </span> </p> </td> 
   <td colname="col3"> <p>選擇電子郵件設定。 可能的值︰ </p> <p> 
     <ul id="ul_0EEDAE11B7CD4C53A6E4B2B8CB2CF730"> 
      <li id="li_F235F93828594ED78C6D464440F953FF"> <span class="codeph"> 全部</span> </li> 
      <li id="li_59E14E7EBFA64432A5FAC15DA21A0521"> <span class="codeph"> 錯誤</span> </li> 
      <li id="li_BFE0B52CADD14CC1BA1AF42AB0AA1CE1"> <span class="codeph"> ErrorAndWarning</span> </li> 
      <li id="li_BE3AA67E14FB487B8B9CD6EF3D58824C"> <span class="codeph"> JobCompletion</span> </li> 
      <li id="li_409C68AD0D244975BFB86B08609E0146"> <span class="codeph"> 無</span> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> clientId</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string  </span> </p> </td> 
   <td colname="col3"> <p>指定啟動匯出請求之用戶端或客戶的IP位址。 </p> <p> <p>注意： 此參數目前未主動填入，且嚴格保留供日後使用。 </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

對於提供`fmt=convert`和`is_modifier`和`macro`的ExportJob請求，目標檔案採用`macro`提供的格式。 例如：

```
input_file = fileToExport.jpg
is_modifer = &fmt=png
macro=$test$ 
output_file = fileToExport.tiff
```

