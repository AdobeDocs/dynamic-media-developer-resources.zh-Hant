---
description: Jpeg品質。 指定JPEG編碼屬性以控制壓縮級別。 這進而會改變檔案大小（回覆資料的量），以及間接地改變產生影像的視覺品質。
solution: Experience Manager
title: qlt
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 8801a650-303c-47a3-8136-c8b2b7a80e9d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 15%

---

# qlt{#qlt}

Jpeg品質。 指定JPEG編碼屬性以控制壓縮級別。 這進而會改變檔案大小（回覆資料的量），以及間接地改變產生影像的視覺品質。

` qlt= *``*[, *`質量色度`*]`

<table id="simpletable_D080D15922CE4EF4B707282A4D45739A"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 品質  </span> </span> </p> </td> 
  <td class="stentry"> <p>JPEG編碼質量(1..100 int)。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 色度  </span> </span> </p> </td> 
  <td class="stentry"> <p>JPEG色度下採樣(0=normal, 1=disable);可選，預設為0。 </p> </td> 
 </tr> 
</table>

僅在`fmt=jpg`時使用。 忽略

較高的值會增加檔案大小並提高品質，較低的值則會減少檔案大小並降低肉眼能感知的影像品質。高於 90 的值所產生的影像通常與未壓縮的影像幾乎沒有差別。

設定`chroma`標誌以禁用典型JPEG編碼器採用的RGB色度下採樣。 當邊緣由色相的變化而不是亮度的變化來定義時，這可以增加影像中邊緣的感知的銳度。 設定此標幟可能會導致檔案大小略有增加。 如果文字看起來有點模糊，請試用此設定。

`chroma` 如果輸出像素類型為CMYK或灰色，則會忽略。

## 範例 {#section-a6c263f15c29424a86ef267c96a6630a}

[!DNL http://server/is/agm/myRootId/myImageId?fmt=jpg&qlt=80]
