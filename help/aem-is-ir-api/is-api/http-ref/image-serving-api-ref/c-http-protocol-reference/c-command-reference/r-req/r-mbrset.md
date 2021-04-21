---
description: 多位元速率資料。
solution: Experience Manager
title: mbrSet
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 0%

---


# mbrSet{#mbrset}

多位元速率資料。

`req=mbrSet[,text|xml[, *`編`*]][&fmt= *`碼fmtType`*]`

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

傳回文字或xml回應，其中包含與網路ID相關之視訊集中之有效視訊項目對應的URL（及對應位元速率）清單。

先前要求有效視訊項目包含`catalog::VideoBitRate`值的要求現已放寬。 該條目可包含&#x200B;`catalog::VideoBitRate`*或* `catalog::AudioBitRate`*或* `catalog::TotalStreamBitRate`的值。 只需定義其中一項，視訊項目才能有效。 請注意，`catalog::Path`和有效視訊副檔名的要求並未變更。

回應的目的是供Apple和Flash串流伺服器使用，因此在結構上符合這些規格。 URL是使用前置詞`attribute::HttpAppleStreamingContext`和`attribute::HttpFlashStreamingContext`生成的。

m3u8回應僅包含mp4檔案（如果有）。 如果沒有mp4檔案，則這些回應僅包含f4v檔案。 如果沒有mp4檔案或f4v檔案，則響應為空。

f4m回應只包含f4v檔案（如果有的話）。 如果沒有f4v檔案，則這些回應僅包含mp4檔案。 如果沒有f4v檔案或mp4檔案，則回應為空。

f4m/m3u8響應中顯示的位速率與`catalog::TotalStreamBitRate`中的值（轉換為適當的單位）相對應。 如果未定義`catalog::TotalStreamBitRate`，則使用`catalog::VideoBitRate`和`catalog::AudioBitRate`的總和。

HTTP響應基於`catalog::NonImgExpiration`可以與TTL進行快取。
