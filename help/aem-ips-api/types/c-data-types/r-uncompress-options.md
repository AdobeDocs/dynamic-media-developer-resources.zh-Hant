---
description: 上傳設定，將ZIP和TAR檔案作為主要資產處理（無），或擷取及上傳其內容（取消壓縮）。
solution: Experience Manager
title: UnCompressOptions
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 89222959-3701-4ea6-bcae-98ceec93764f
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 7%

---

# UnCompressOptions{#uncompressoptions}

上傳設定，將ZIP和TAR檔案作為主要資產處理（無），或擷取及上傳其內容（取消壓縮）。

>[!NOTE]
>
>`None` 為預設值。

## 參數 {#section-10e49e27f60743da970a4ff1c4587eab}

<table id="table_89C2F7CDB24848459E47F1F7F58D91BA"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 名稱 </th> 
   <th colname="col2" class="entry"> 類型 </th> 
   <th colname="col3" class="entry"> 說明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 過程</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>控制ZIP和TAR封存檔案處理。 提供2個選項： 
     <ul id="ul_F34E2F3B9B74450CA7E76BD9FD7137C2">
      <li id="li_E982468ED814446593B0C0A3F3D729FB"><span class="codeph"> 無：</span> 以主要資產處理。 </li>
      <li id="li_4A45DA99592B4EF7A1FE0A946A835104"><span class="codeph"> 取消壓縮：</span> 擷取和處理內容。 </li>
     </ul><p>注意：字串常數區分大小寫。 使用<span class="codeph"> UnCompress</span>，而不是<span class="codeph">解壓縮</span>或<span class="codeph"> unCompress</span>。 </p></p> </td> 
  </tr> 
 </tbody> 
</table>

## 範例 {#section-48fd14af768a436284c31692038579a8}

```
 <!-- uncompress zip/tar/gzip files -->
            <element name="unCompressOptions" type="types:UnCompressOptions" minOccurs="0"/>
    <complexType name="UnCompressOptions">
        <sequence>
            <!-- Options: None (default),UnCompress -->
            <element name="process" type="xsd:string"/>
        </sequence>
    </complexType>
```

## 使用者 {#section-b2a829cf5511412e968bb2000f85cc31}

`unCompressionOptions`類型由：

* [UploadDirectoryJob](../../types/c-data-types/r-upload-directory-job.md#reference-e707ebf53b074c49ad983d1886e0bbb6)
* [UploadPostJob](../../types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4)
* [UploadUrlsJob](../../types/c-data-types/r-upload-urls-job.md#reference-8e9bc895268c4321b233dbeadc990398)
