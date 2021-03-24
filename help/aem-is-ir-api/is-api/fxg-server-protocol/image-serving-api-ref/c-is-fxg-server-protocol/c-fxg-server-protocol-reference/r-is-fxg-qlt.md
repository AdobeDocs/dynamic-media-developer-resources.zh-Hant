---
description: Jpeg品質。 指定JPEG編碼屬性以控制壓縮級別。 這進而會改變檔案大小（回覆資料的量），並間接地改變所產生影像的視覺品質。
solution: Experience Manager
title: qlt
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 15%

---


# qlt{#qlt}

Jpeg品質。 指定JPEG編碼屬性以控制壓縮級別。 這進而會改變檔案大小（回覆資料的量），並間接地改變所產生影像的視覺品質。

` qlt= *`品`*[, *`質`*]`

<table id="simpletable_D080D15922CE4EF4B707282A4D45739A"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 質量  </span> </span> </p> </td> 
  <td class="stentry"> <p>JPEG編碼品質(1...100 int)。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 色度  </span> </span> </p> </td> 
  <td class="stentry"> <p>JPEG色度下採樣(0=normal, 1=disable);可選，預設為0。 </p> </td> 
 </tr> 
</table>

僅在`fmt=jpg`時使用。 否則忽略

較高的值會增加檔案大小並提高品質，較低的值則會減少檔案大小並降低肉眼能感知的影像品質。高於 90 的值所產生的影像通常與未壓縮的影像幾乎沒有差別。

設定`chroma`標幟，以停用典型JPEG編碼器所採用的RGB色度下採樣。 當邊緣由色相而不是亮度的變化來定義時，這可以增加影像中邊緣的感知清晰度。 設定此標幟可能會使檔案大小稍微增加。 如果文字看起來有點模糊，請嘗試使用此設定。

`chroma` 如果輸出像素類型是CMYK或灰色，則會忽略此值。

## 範例 {#section-a6c263f15c29424a86ef267c96a6630a}

[!DNL http://server/is/agm/myRootId/myImageId?fmt=jpg&qlt=80]
