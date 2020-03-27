---
description: 產生視訊的縮圖影像。
seo-description: 產生視訊的縮圖影像。
seo-title: MediaOptions
solution: Experience Manager
title: MediaOptions
topic: Scene7 Image Production System API
uuid: 4de59678-1bef-484c-9a43-ded531537aeb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# MediaOptions{#mediaoptions}

產生視訊的縮圖影像。

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
   <td colname="col1"> <span class="codeph"> 視訊 <span class="varname"> 編碼預設集陣列</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：HandleArray</span> </td> 
   <td colname="col3">PropertySet控點的陣 <span class="codeph"> 列</span> ，可參照視訊編碼預設集來轉碼視訊。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> generateThumbnail</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 若為true，則會擷取視訊的第一個影格，並用作縮圖影像。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 縮 <span class="varname"> 圖選項</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：縮圖選項</span> </td> 
   <td colname="col3">選填。可讓您選擇特定影格做為縮圖影像。 <p>若要指定縮圖影像，請傳入您要使用之影格的時間（以視訊開始時的毫秒為單位）。 值範圍從0到視訊結尾。 <p>注意：如果您指定的時間不正確，請 <span class="codeph"> 產生縮圖</span> ，預設為true。 </p></p><p>請參閱 <a href="../../types/c-data-types/r-thumbnail-options.md#reference-370088b0a4ce4096b9b3e5489a368b5c" format="dita" scope="local"> 縮圖選項</a>。 </p></td> 
  </tr> 
 </tbody> 
</table>

## 範例 {#section-a9356de782d74af6933c39fa7ad12212}

```
<complexType name="MediaOptions">
        <sequence>
            <element name="videoEncodingPresetsArray" type="types:HandleArray" minOccurs="0"/>
            <element name="generateThumbnail" type="xsd:boolean" minOccurs="0"/>
            <element name="thumbnailOptions" type="types:ThumbnailOptions" minOccurs="0"/>
        </sequence>
    </complexType>
```

## 使用者 {#section-87cb83407198432c95eaa2db9f12f9db}

該 `mediaOptions` 類型由：

* [UploadDirectoryJob](../../types/c-data-types/r-upload-directory-job.md#reference-e707ebf53b074c49ad983d1886e0bbb6)
* [UploadPostJob](../../types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4)
* [UploadURLsJob](../../types/c-data-types/r-upload-urls-job.md#reference-8e9bc895268c4321b233dbeadc990398)

