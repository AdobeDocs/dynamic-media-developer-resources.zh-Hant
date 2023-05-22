---
description: 生成視頻的縮略圖。
solution: Experience Manager
title: 媒體選項
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f37d935d-fe74-4878-8477-d2144d58d982
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 7%

---

# [!DNL MediaOptions]{#mediaoptions}

生成視頻的縮略圖。

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> videoEncodingPresetsArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：HandleArray</span> </td> 
   <td colname="col3">一組 <span class="codeph"> 屬性集</span> 處理引用視頻編碼預置以進行視頻代碼轉換。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> generateThumbnail</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 當為true時，提取視頻的第一幀並將其用作縮略圖。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 縮略圖選項</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：縮略圖選項</span> </td> 
   <td colname="col3">選擇性. 允許您選擇特定視頻幀作為縮略圖。 <p>要指定縮略圖，請在要使用的幀的時間（從視頻啟動開始的毫秒）內傳遞。 值範圍從0到視頻結尾。 <p>注：如果指定時間不正確， <span class="codeph"> generateThumbnail</span> 預設為true。 </p></p><p>請參閱 <a href="../../types/c-data-types/r-thumbnail-options.md#reference-370088b0a4ce4096b9b3e5489a368b5c" format="dita" scope="local"> 縮略圖選項</a>。 </p></td> 
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

的 `mediaOptions` 類型由：

* [上載目錄作業](../../types/c-data-types/r-upload-directory-job.md#reference-e707ebf53b074c49ad983d1886e0bbb6)
* [上載後作業](../../types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4)
* [上載URL作業](../../types/c-data-types/r-upload-urls-job.md#reference-8e9bc895268c4321b233dbeadc990398)
