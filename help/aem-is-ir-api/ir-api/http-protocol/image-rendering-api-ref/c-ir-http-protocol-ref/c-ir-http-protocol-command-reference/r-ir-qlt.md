---
title: qlt
description: Jpeg品質。 指定JPEG編碼屬性來控制壓縮等級。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 49af2620-081f-4bcc-8245-5aa6bab89a05
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 7%

---

# qlt{#qlt}

Jpeg品質。 指定JPEG編碼屬性來控制壓縮等級。

` qlt= *`品質`*[. *`色度`*]`

<table id="simpletable_A245B6A3D2374A6A89DE63A5621CFEC0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname">品質</span> </p> </td> 
  <td class="stentry"> <p>JPEG編碼品質（1分100秒） </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname">色度</span> </p> </td> 
  <td class="stentry"> <p>JPEG色度向下取樣（0=一般，1=停用）；選用，預設為0。 </p> </td> 
 </tr> 
</table>

指定JPEG編碼屬性來控制壓縮等級。 反過來，這會改變檔案大小（回覆資料量），並間接改變結果影像的視覺品質。

較高的&#x200B;*`quality`*&#x200B;值會增加檔案大小和品質，較低的值會減少檔案大小並降低感知到的影像品質。 高於 90 的值所產生的影像通常與未壓縮的影像幾乎沒有差別。

設定&#x200B;*`chroma`*&#x200B;旗標以停用典型JPEG編碼器採用的色度縮減取樣。 當邊緣是由色相而非亮度變更所定義時，此設定可能會增加影像中邊緣的感知銳利度。 設定此旗標可能會導致檔案大小稍微增加。 如果文字看起來有點模糊，請嘗試使用此設定。

## 屬性 {#section-897b61c786dd4230a2c5807f2f40e722}

可能發生在請求中的任何位置。

如果輸出影像格式不支援JPEG壓縮，則忽略。 如需支援JPEG壓縮的輸出影像格式清單，請參閱`fmt=`的說明。

## 預設 {#section-1c1257df843c475bbac6aadaffcb6347}

`attribute::JpegQuality`

## 另請參閱 {#section-61871fbded3a42f68cf3bdcaed35eae1}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c)，[attribute：：JpegQuality](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-jpegquality.md#reference-d86fc5ad18bb436891efdbe1f98fea50)
