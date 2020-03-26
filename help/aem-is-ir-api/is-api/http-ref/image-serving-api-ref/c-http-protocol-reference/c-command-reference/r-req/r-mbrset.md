---
description: 多位元速率資料。
seo-description: 多位元速率資料。
seo-title: mbrSet
solution: Experience Manager
title: mbrSet
topic: Scene7 Image Serving - Image Rendering API
uuid: 829c44ce-c66a-49a9-ba69-9e8e94ef8921
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# mbrSet{#mbrset}

多位元速率資料。

`req=mbrSet[,text|xml[, *`編`*]][&fmt= *`碼fmtType`*]`

<table id="simpletable_D2B8704E09B34337870A257CD7CB5C56"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 編碼</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8| UTF-16| UTF-16LE| UTF-16BE| ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> fmtType</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> f4m| m3u8</span> </p></td> 
 </tr> 
</table>

傳回文字或xml回應，其中包含與網路ID相關之視訊集中之有效視訊項目對應的URL（及對應位元速率）清單。

先前要求有效視訊項目包含值的要求 `catalog::VideoBitRate` 現已放寬。 條目可包含或 `catalog::VideoBitRate`*或&#x200B;*`catalog::AudioBitRate`*的值*`catalog::TotalStreamBitRate`。 只需定義其中一項，視訊項目才能有效。 請注意，對有效視 `catalog::Path` 訊檔案副檔名和要求並未變更。

回應的用途是供Apple和Flash串流伺服器使用，因此在結構上符合這些規格。 URL是使用前置詞和 `attribute::HttpAppleStreamingContext` 生成 `attribute::HttpFlashStreamingContext`的。

m3u8回應僅包含mp4檔案（如果有）。 如果沒有mp4檔案，則這些回應僅包含f4v檔案。 如果沒有mp4檔案或f4v檔案，則響應為空。

f4m回應只包含f4v檔案（如果有的話）。 如果沒有f4v檔案，則這些回應僅包含mp4檔案。 如果沒有f4v檔案或mp4檔案，則回應為空。

f4m/m3u8回應中顯示的位元速率對應於 `catalog::TotalStreamBitRate` （轉換為適當單位）中的值。 如 `catalog::TotalStreamBitRate` 果未定義，則使用和 `catalog::VideoBitRate` 的 `catalog::AudioBitRate` 總和。

The HTTP response is cacheable with the TTL based on `catalog::NonImgExpiration`.
