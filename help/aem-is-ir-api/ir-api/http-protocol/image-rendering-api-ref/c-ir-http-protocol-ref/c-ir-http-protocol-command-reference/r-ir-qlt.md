---
description: Jpeg品質。 指定JPEG編碼屬性以控制壓縮級別。
solution: Experience Manager
title: qlt
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 7%

---


# qlt{#qlt}

Jpeg品質。 指定JPEG編碼屬性以控制壓縮級別。

` qlt= *`品`*[. *`質`*]`

<table id="simpletable_A245B6A3D2374A6A89DE63A5621CFEC0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 品質 </span> </p> </td> 
  <td class="stentry"> <p>JPEG編碼品質(1...100) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 色度  </span> </p> </td> 
  <td class="stentry"> <p>JPEG色度下採樣(0=normal, 1=disable);可選，預設為0。 </p> </td> 
 </tr> 
</table>

指定JPEG編碼屬性以控制壓縮級別。 這進而會改變檔案大小（回覆資料的量），並間接地改變所產生影像的視覺品質。

*`quality`*&#x200B;值越高，檔案大小和品質就越高，值越低，檔案大小就越小，影像品質也越明顯。 高於 90 的值所產生的影像通常與未壓縮的影像幾乎沒有差別。

設定&#x200B;*`chroma`*&#x200B;標幟，以停用典型JPEG編碼器所採用的色度下取樣。 當邊緣由色相而不是亮度的變化來定義時，這可以增加影像中邊緣的感知清晰度。 設定此標幟可能會使檔案大小稍微增加。 如果文字看起來有點模糊，請嘗試使用此設定。

## 屬性 {#section-897b61c786dd4230a2c5807f2f40e722}

可能發生在請求中的任何位置。

如果輸出影像格式不支援JPEG壓縮，則忽略。 有關支援JPEG壓縮的輸出影像格式的清單，請參閱`fmt=`的說明。

## 預設 {#section-1c1257df843c475bbac6aadaffcb6347}

`attribute::JpegQuality`

## 另請參閱 {#section-61871fbded3a42f68cf3bdcaed35eae1}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c)，屬 [性：:JpegQuality](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-jpegquality.md#reference-d86fc5ad18bb436891efdbe1f98fea50)
