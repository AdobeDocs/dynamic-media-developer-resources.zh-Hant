---
description: 作業類型，允許授權匯出先前上傳的檔案。
seo-description: 作業類型，允許授權匯出先前上傳的檔案。
seo-title: ExportJob
solution: Experience Manager
title: ExportJob
topic: Scene7 Image Production System API
uuid: 439e3dd8-85b8-4f5b-abf8-8cc5a3f59fe6
translation-type: tm+mt
source-git-commit: 26fb6212c3106deb7b088020d9f2993e40dec20b

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
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> assetHandleArray</span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 類型：HandleArray</span> </p> </td> 
   <td colname="col3" valign="top"> <p>需要 <span class="codeph"> 匯出的</span> assetHandle的清單。 請參 <a href="../../types/c-data-types/r-handle-array.md#reference-1b93fefb5477459faf9253b54349b5f9" type="reference" format="dita" scope="local"> 閱HandleArray</a>。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> fmt</span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string </span> </p> </td> 
   <td colname="col3"> <p>指定導出的類 <span class="codeph"> 型。可能的值</span>:[orig, convert] </p> <p> 
     <ul id="ul_16EF4B14100C4C7AA464CA9CF7F11D1C"> 
      <li id="li_DAB2844CC55145C88A18A1F8EC4527F9">如果 <span class="codeph"> fmt=orig</span>，則資產將導出為原始資產 </li> 
      <li id="li_07F2F8D159934D889FDC1022AB12B564">如果 <span class="codeph"> fmt=convert</span>，則資產將轉換為is_modifer或宏輸入參數中 <span class="codeph"> 指定的格式</span> , <span class="codeph"> 即</span> 可 </li> 
     </ul> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> is_modifier</span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string </span> </p> </td> 
   <td colname="col3"> <p>指定 <span class="codeph"> ImageServer</span> 轉譯URL字串，此字串會附加至ExportJob轉 <span class="codeph"> 換請求</span> 。 </p> <p>如需傳送IS修飾 <a href="https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/" scope="external" format="html"> 詞的詳細資訊</a> ，請參閱IS檔案。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 宏</span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string </span> </p> </td> 
   <td colname="col3"> <p></p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> 電子 <span class="varname"> 郵件設定</span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string </span> </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> 用戶 <span class="varname"> 端ID</span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string </span> </p> </td> 
   <td colname="col3"> <p>指定啟動匯出請求之用戶端或客戶的IP位址。 </p> <p> <p>注意： 此參數目前未主動填入，且嚴格保留供日後使用。 </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

對於同時提供和 `fmt=convert` 同時提供 `is_modifier` 的 `macro` ExportJob請求，目標檔案遵守由提供的格式 `macro`。 例如：

```
input_file = fileToExport.jpg
is_modifer = &fmt=png
macro=$test$ 
output_file = fileToExport.tiff
```

