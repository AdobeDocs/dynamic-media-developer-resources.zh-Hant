---
title: qlt
description: Jpeg品質。 指定JPEG編碼屬性來控制壓縮等級。 這進而會改變檔案大小（回覆資料量），並間接改變結果影像的視覺品質。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8801a650-303c-47a3-8136-c8b2b7a80e9d
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 15%

---

# qlt{#qlt}

Jpeg品質。 指定JPEG編碼屬性來控制壓縮等級。 這進而會改變檔案大小（回覆資料量），並間接改變結果影像的視覺品質。

` qlt= *`品質`*[, *`色度`*]`

<table id="simpletable_D080D15922CE4EF4B707282A4D45739A"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">品質</span> </span> </p> </td> 
  <td class="stentry"> <p>JPEG編碼品質(1...100 int)。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">色度</span> </span> </p> </td> 
  <td class="stentry"> <p>JPEG色度向下取樣（0=一般，1=停用）；選用，預設為0。 </p> </td> 
 </tr> 
</table>

僅在`fmt=jpg`時使用。 已忽略，否則

較高的值會增加檔案大小並提高品質，較低的值則會減少檔案大小並降低肉眼能感知的影像品質。高於 90 的值所產生的影像通常與未壓縮的影像幾乎沒有差別。

設定`chroma`旗標以停用典型RGB編碼器所使用的JPEG色度縮減取樣。 當邊緣是由色相而非亮度的變化所定義時，這可能會增加影像中邊緣的感知銳利度。 設定此旗標可能會導致檔案大小稍微增加。 如果文字看起來有點模糊，請嘗試使用此設定。

如果輸出畫素型別為CMYK或灰色，則會忽略`chroma`。

## 範例 {#section-a6c263f15c29424a86ef267c96a6630a}

`http://server/is/agm/myRootId/myImageId?fmt=jpg&qlt=80`
