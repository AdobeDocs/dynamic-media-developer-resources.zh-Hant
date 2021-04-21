---
description: JPEG品質。 指定JPEG編碼屬性以控制壓縮級別。 這進而會改變檔案大小（回覆資料的量），並間接地改變所產生影像的視覺品質。
solution: Experience Manager
title: qlt
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 6%

---


# qlt{#qlt}

JPEG品質。 指定JPEG編碼屬性以控制壓縮級別。 這進而會改變檔案大小（回覆資料的量），並間接地改變所產生影像的視覺品質。

` qlt= *`品`*[, *`質`*]`

<table id="simpletable_FB8090D4BEBF42FD83A64A7AAB6D7F92"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 品質 </span> </p> </td> 
  <td class="stentry"> <p>JPEG編碼品質(1...100 int)。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 色度  </span> </p> </td> 
  <td class="stentry"> <p>JPEG色度下採樣(0=normal, 1=disable);可選，預設為0。 </p> </td> 
 </tr> 
</table>

*`quality`*&#x200B;值越高，檔案大小和品質就越高，值越低，檔案大小就越小，影像品質也越明顯。 高於 90 的值所產生的影像通常與未壓縮的影像幾乎沒有差別。

設定&#x200B;*`chroma`*&#x200B;標幟，以停用典型JPEG編碼器所採用的RGB色度下採樣。 當邊緣由色相而不是亮度的變化來定義時，這可以增加影像中邊緣的感知清晰度。 設定此標幟可能會使檔案大小稍微增加。 如果文字看起來有點模糊，請嘗試使用此設定。

## 屬性 {#section-925a44cbdc9042db8d4eb149cd073d21}

請求屬性。 不論目前的圖層設定如何，都適用。 如果輸出影像檔案格式不支援JPEG編碼，則忽略。 有關輸出影像格式支援`qlt=`的資訊，請參閱`fmt=`的說明。

*`chroma`* 如果輸出像素類型是CMYK或灰色，則會忽略此值。

## 預設 {#section-0d8aa45d84df49e6b846596bbaf7f740}

`attribute::JpegQuality`

## 範例 {#section-d7d33871d401433aa51d028823eae7a9}

降低透過低頻寬連線的傳輸品質：

`http://server/myRoodId/myImageId?qlt=60&wid=300`

提高高頻寬連線的品質：

`http://server/myRootId/myImageId?qlt=95,1&wid=300`

## 另請參閱 {#section-0074a060bb314ddfa7f4ed23be976507}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) ，屬 [性：:JpegQuality](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-jpegquality.md#reference-4a879e7c46024c8a898a9fd226f9eb09)
