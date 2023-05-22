---
description: JPEG質量。 指定JPEG編碼屬性以控制壓縮級別。 這進而會改變檔案大小（回復資料的量），並間接地改變結果影像的視覺質量。
solution: Experience Manager
title: QLT
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c2a611a8-f331-4e01-a262-34340ce67b21
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 6%

---

# QLT{#qlt}

JPEG質量。 指定JPEG編碼屬性以控制壓縮級別。 這進而會改變檔案大小（回復資料的量），並間接地改變結果影像的視覺質量。

` qlt= *`質量`*[, *`色度`*]`

<table id="simpletable_FB8090D4BEBF42FD83A64A7AAB6D7F92"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 品質 </span> </p> </td> 
  <td class="stentry"> <p>JPEG編碼質量(1...100 int)。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 色度 </span> </p> </td> 
  <td class="stentry"> <p>JPEG色度下採樣(0=normal,1=disable);可選，預設值為0。 </p> </td> 
 </tr> 
</table>

更高 *`quality`* 值增加了檔案大小和質量，較低的值減小了檔案大小並降低了感知影像質量。 高於 90 的值所產生的影像通常與未壓縮的影像幾乎沒有差別。

設定 *`chroma`* 標誌，以禁用典型RGB編碼器使用的JPEG色度下採樣。 當邊緣由色相而不是亮度的變化來定義時，這可以增加影像中邊緣的感知銳度。 設定此標誌可能會導致檔案大小略有增加。 如果文本看起來有點模糊，請嘗試此設定。

## 屬性 {#section-925a44cbdc9042db8d4eb149cd073d21}

請求屬性。 應用，與當前圖層設定無關。 如果輸出影像檔案格式不支援JPEG編碼，則忽略。 請參閱 `fmt=` 有關輸出影像格式支援的資訊 `qlt=`。

*`chroma`* 如果輸出像素類型為CMYK或灰色，則忽略。

## 預設 {#section-0d8aa45d84df49e6b846596bbaf7f740}

`attribute::JpegQuality`

## 範例 {#section-d7d33871d401433aa51d028823eae7a9}

通過低頻寬連接降低傳輸質量：

`http://server/myRoodId/myImageId?qlt=60&wid=300`

提高高頻寬連接的質量：

`http://server/myRootId/myImageId?qlt=95,1&wid=300`

## 另請參閱 {#section-0074a060bb314ddfa7f4ed23be976507}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) 。 [屬性：:JpegQuality](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-jpegquality.md#reference-4a879e7c46024c8a898a9fd226f9eb09)
