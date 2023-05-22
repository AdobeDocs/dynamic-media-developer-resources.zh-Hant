---
description: Jpeg品質。 指定JPEG編碼屬性以控制壓縮級別。 這進而會改變檔案大小（回復資料的量），並間接地改變結果影像的視覺質量。
solution: Experience Manager
title: QLT
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8801a650-303c-47a3-8136-c8b2b7a80e9d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 15%

---

# QLT{#qlt}

Jpeg品質。 指定JPEG編碼屬性以控制壓縮級別。 這進而會改變檔案大小（回復資料的量），並間接地改變結果影像的視覺質量。

` qlt= *`質量`*[, *`色度`*]`

<table id="simpletable_D080D15922CE4EF4B707282A4D45739A"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 質量 </span> </span> </p> </td> 
  <td class="stentry"> <p>JPEG編碼質量(1...100 int)。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 色度 </span> </span> </p> </td> 
  <td class="stentry"> <p>JPEG色度下採樣(0=normal,1=disable);可選，預設值為0。 </p> </td> 
 </tr> 
</table>

僅在 `fmt=jpg`。 忽略（否則）

較高的值會增加檔案大小並提高品質，較低的值則會減少檔案大小並降低肉眼能感知的影像品質。高於 90 的值所產生的影像通常與未壓縮的影像幾乎沒有差別。

設定 `chroma` 標誌，以禁用典型RGB編碼器使用的JPEG色度下採樣。 當邊緣由色相而不是亮度的變化來定義時，這可以增加影像中邊緣的感知銳度。 設定此標誌可能會導致檔案大小略有增加。 如果文本看起來有點模糊，請嘗試此設定。

`chroma` 如果輸出像素類型為CMYK或灰色，則忽略。

## 範例 {#section-a6c263f15c29424a86ef267c96a6630a}

[!DNL http://server/is/agm/myRootId/myImageId?fmt=jpg&qlt=80]
