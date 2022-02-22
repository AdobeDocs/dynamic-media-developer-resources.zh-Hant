---
title: QLT
description: Jpeg品質。 指定JPEG編碼屬性以控制壓縮級別。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 49af2620-081f-4bcc-8245-5aa6bab89a05
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 7%

---

# QLT{#qlt}

Jpeg品質。 指定JPEG編碼屬性以控制壓縮級別。

` qlt= *`質量`*[. *`色度`*]`

<table id="simpletable_A245B6A3D2374A6A89DE63A5621CFEC0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 品質 </span> </p> </td> 
  <td class="stentry"> <p>JPEG編碼質量(1..100) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 色度 </span> </p> </td> 
  <td class="stentry"> <p>JPEG色度下採樣(0=normal,1=disable);可選，預設值為0。 </p> </td> 
 </tr> 
</table>

指定JPEG編碼屬性以控制壓縮級別。 反過來，這會改變檔案大小（回復資料的量），並間接地改變結果影像的視覺質量。

更高 *`quality`* 值增加了檔案大小和質量，較低的值減小了檔案大小並降低了感知影像質量。 高於 90 的值所產生的影像通常與未壓縮的影像幾乎沒有差別。

設定 *`chroma`* 標誌，以禁用典型JPEG編碼器使用的色度下採樣。 當邊緣由色相而不是亮度的變化來定義時，此設定可增加影像中邊緣的感知銳度。 設定此標誌可能會導致檔案大小略有增加。 如果文本看起來有點模糊，請嘗試此設定。

## 屬性 {#section-897b61c786dd4230a2c5807f2f40e722}

請求中的任何位置都可能發生。

如果輸出影像格式不支援JPEG壓縮，則忽略。 請參閱 `fmt=` 的子菜單。

## 預設 {#section-1c1257df843c475bbac6aadaffcb6347}

`attribute::JpegQuality`

## 另請參閱 {#section-61871fbded3a42f68cf3bdcaed35eae1}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c)。 [屬性：:JpegQuality](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-jpegquality.md#reference-d86fc5ad18bb436891efdbe1f98fea50)
