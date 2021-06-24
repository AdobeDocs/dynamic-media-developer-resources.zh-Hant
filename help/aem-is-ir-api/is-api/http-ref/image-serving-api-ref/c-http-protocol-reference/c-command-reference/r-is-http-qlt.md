---
description: JPEG質量。 指定JPEG編碼屬性以控制壓縮級別。 這進而會改變檔案大小（回覆資料的量），以及間接地改變產生影像的視覺品質。
solution: Experience Manager
title: qlt
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: c2a611a8-f331-4e01-a262-34340ce67b21
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 6%

---

# qlt{#qlt}

JPEG質量。 指定JPEG編碼屬性以控制壓縮級別。 這進而會改變檔案大小（回覆資料的量），以及間接地改變產生影像的視覺品質。

` qlt= *``*[, *`質量色度`*]`

<table id="simpletable_FB8090D4BEBF42FD83A64A7AAB6D7F92"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 品質 </span> </p> </td> 
  <td class="stentry"> <p>JPEG編碼質量(1..100 int)。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 色度  </span> </p> </td> 
  <td class="stentry"> <p>JPEG色度下採樣(0=normal, 1=disable);可選，預設為0。 </p> </td> 
 </tr> 
</table>

*`quality`*&#x200B;值越高，檔案大小和質量越高，值越低，檔案大小越小，影像質量越低。 高於 90 的值所產生的影像通常與未壓縮的影像幾乎沒有差別。

設定&#x200B;*`chroma`*&#x200B;標誌以禁用典型JPEG編碼器採用的RGB色度下採樣。 當邊緣由色相的變化而不是亮度的變化來定義時，這可以增加影像中邊緣的感知的銳度。 設定此標幟可能會導致檔案大小略有增加。 如果文字看起來有點模糊，請試用此設定。

## 屬性 {#section-925a44cbdc9042db8d4eb149cd073d21}

要求屬性。 無論目前的層設定為何皆適用。 如果輸出影像檔案格式不支援JPEG編碼，則忽略。 有關輸出影像格式支援`qlt=`的資訊，請參閱`fmt=`的說明。

*`chroma`* 如果輸出像素類型為CMYK或灰色，則會忽略。

## 預設 {#section-0d8aa45d84df49e6b846596bbaf7f740}

`attribute::JpegQuality`

## 範例 {#section-d7d33871d401433aa51d028823eae7a9}

通過低頻寬連接降低傳輸質量：

`http://server/myRoodId/myImageId?qlt=60&wid=300`

提高高頻寬連接的質量：

`http://server/myRootId/myImageId?qlt=95,1&wid=300`

## 另請參閱 {#section-0074a060bb314ddfa7f4ed23be976507}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) ，屬 [性：:JpegQuality](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-jpegquality.md#reference-4a879e7c46024c8a898a9fd226f9eb09)
