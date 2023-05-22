---
description: 多位速率資料。
solution: Experience Manager
title: mbr集
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0568a4a1-7d6a-453e-83bc-05c0cde0c0f8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 0%

---

# mbr集{#mbrset}

多位速率資料。

`req=mbrSet[,text|xml[, *`編碼`*]][&fmt= *`fmt類型`*]`

<table id="simpletable_D2B8704E09B34337870A257CD7CB5C56"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 編碼</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> fmt類型</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> f4m | m3u8</span> </p></td> 
 </tr> 
</table>

返回文本或xml響應，該響應包含與與網路路徑ID關聯的視頻集中的有效視頻條目對應的URL（和相應的比特率）清單。

先前要求有效視頻條目包含 `catalog::VideoBitRate` 現在已經放鬆了。 條目可包含 `catalog::VideoBitRate`*或* `catalog::AudioBitRate`*或* `catalog::TotalStreamBitRate`。 只需定義其中一個視頻條目才能有效。 請注意， `catalog::Path` 並且有效的視頻檔案副檔名未更改。

響應旨在供Apple和Flash流伺服器使用，因此在結構上符合這些規範。 使用前置詞生成URL `attribute::HttpAppleStreamingContext` 和 `attribute::HttpFlashStreamingContext`。

m3u8響應僅包含mp4檔案（如果視頻集中存在）。 如果沒有mp4檔案，則這些響應僅包含f4v檔案。 如果沒有mp4檔案或f4v檔案，則響應為空。

f4m響應僅包含f4v檔案（如果視頻集中存在）。 如果沒有f4v檔案，則這些響應僅包含mp4檔案。 如果沒有f4v檔案或mp4檔案，則響應為空。

在f4m/m3u8響應中顯示的比特率與中的值相對應 `catalog::TotalStreamBitRate` （轉換為相應單位）。 如果 `catalog::TotalStreamBitRate` 未定義， `catalog::VideoBitRate` 和 `catalog::AudioBitRate` 的子菜單。

HTTP響應可以與基於的TTL進行快取 `catalog::NonImgExpiration`。
