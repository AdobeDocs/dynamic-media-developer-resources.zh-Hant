---
description: 多位速率資料。
solution: Experience Manager
title: mbrSet
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0568a4a1-7d6a-453e-83bc-05c0cde0c0f8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '264'
ht-degree: 0%

---

# mbrSet{#mbrset}

多位速率資料。

`req=mbrSet[,text|xml[, *``*]][&fmt= *`encodingfmtType`*]`

<table id="simpletable_D2B8704E09B34337870A257CD7CB5C56"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 編碼</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> fmtType</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> f4m | m3u8</span> </p></td> 
 </tr> 
</table>

返回文本或xml響應，該響應包含與與網路路徑ID關聯的視頻集中的有效視頻條目對應的URL清單（和相應的比特率）。

先前要求有效視訊項目包含`catalog::VideoBitRate`值的要求現已放寬。 該條目可以包含&#x200B;`catalog::VideoBitRate`*或* `catalog::AudioBitRate`*或* `catalog::TotalStreamBitRate`的值。 只需定義其中一個，視訊項目才能有效。 請注意，`catalog::Path`和有效視訊檔案副檔名的要求未變更。

回應旨在供Apple和Flash串流伺服器使用，因此在結構上符合這些規格。 URL是使用前置詞`attribute::HttpAppleStreamingContext`和`attribute::HttpFlashStreamingContext`產生。

m3u8回應僅包含mp4檔案（如果視訊集中有）。 如果沒有mp4檔案，則這些響應僅包含f4v檔案。 如果不存在mp4檔案或f4v檔案，則響應為空。

f4m回應只會包含視訊集中存在的f4v檔案。 如果沒有f4v檔案，則這些響應僅包含mp4檔案。 如果沒有f4v檔案或mp4檔案，則響應為空。

f4m/m3u8響應中顯示的位速率對應於`catalog::TotalStreamBitRate`中的值（轉換為相應的單位）。 如果未定義`catalog::TotalStreamBitRate`，則使用`catalog::VideoBitRate`和`catalog::AudioBitRate`的總和。

HTTP回應可根據`catalog::NonImgExpiration`與TTL快取。
