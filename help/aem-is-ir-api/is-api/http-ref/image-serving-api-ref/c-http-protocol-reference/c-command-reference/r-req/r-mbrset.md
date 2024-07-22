---
description: 多位元速率資料。
solution: Experience Manager
title: mbrSet
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0568a4a1-7d6a-453e-83bc-05c0cde0c0f8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 0%

---

# mbrSet{#mbrset}

多位元速率資料。

`req=mbrSet[,text|xml[, *`編碼`*]][&fmt= *`fmtType`*]`

<table id="simpletable_D2B8704E09B34337870A257CD7CB5C56"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname">編碼</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> fmtType</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> f4m | m3u8</span> </p></td> 
 </tr> 
</table>

傳回文字或xml回應，其中包含URL （以及對應的位元速率）清單，這些清單會對應到與網路路徑ID相關聯的視訊集內的有效視訊專案。

先前要求有效視訊專案包含`catalog::VideoBitRate`值的要求現已寬鬆。 專案可以包含&#x200B;`catalog::VideoBitRate`*或* `catalog::AudioBitRate`*或* `catalog::TotalStreamBitRate`的值。 只要定義其中一個專案，視訊專案就會有效。 請注意，`catalog::Path`與有效視訊檔副檔名的要求並未變更。

回應旨在供Apple和Flash串流伺服器使用，因此在結構上符合這些規格。 使用前置詞`attribute::HttpAppleStreamingContext`和`attribute::HttpFlashStreamingContext`產生URL。

m3u8回應只包含mp4檔案（如果視訊集中有任何檔案）。 如果沒有mp4檔案，則這些回應只會包含f4v檔案。 如果沒有mp4檔案或f4v檔案，回應會是空的。

f4m回應只包含f4v檔案（如果視訊集中有任何檔案）。 如果沒有f4v檔案，則這些回應只會包含mp4檔案。 如果沒有f4v檔案或mp4檔案，回應會是空的。

顯示在f4m/m3u8回應中的位元速率對應到`catalog::TotalStreamBitRate`中的值（轉換為適當的單位）。 如果未定義`catalog::TotalStreamBitRate`，則會使用`catalog::VideoBitRate`與`catalog::AudioBitRate`的總和。

HTTP回應可使用以`catalog::NonImgExpiration`為基礎的TTL進行快取。
