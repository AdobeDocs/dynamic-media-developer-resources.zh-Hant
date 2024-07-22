---
description: 縮圖型別。 說明如何產生此影像的縮圖。
solution: Experience Manager
title: 縮圖型別
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a90b587d-6893-44e4-8dce-7676bc7eebe3
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 1%

---

# 縮圖型別{#thumbtype}

縮圖型別。 說明如何產生此影像的縮圖。

支援的縮圖型別如下：

<table id="simpletable_874E4190A1DC4FB0AE1B2E3734746527"> 
 <tr class="strow"> 
  <td class="stentry"> <p>裁切(1) </p></td> 
  <td class="stentry"> <p>裁切影像至縮圖外觀比例。 除非縮圖矩形和影像的外觀比例完全相同，否則影像的一部分會被裁切，以確保整個縮圖矩形填滿影像資料。 裁切矩形是使用<span class="codeph">屬性：：ThumbHorizAlign</span>和<span class="codeph">屬性：：ThumbVertAlign</span>放置在影像中。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>符合(2) </p></td> 
  <td class="stentry"> <p>將整個影像調整到縮圖矩形中。 使用<span class="codeph">屬性：：ThumbHorizAlign</span>和<span class="codeph">屬性：：ThumbVertAlign</span>將影像放置在縮圖矩形內，任何額外的空格都會以<span class="codeph">屬性：：ThumbBkgColor</span>填滿。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>紋理(3) </p></td> 
  <td class="stentry"> <p>根據解析度裁切影像。 影像是以<span class="codeph">目錄：：ThumbRes</span>與<span class="codeph">目錄：：Resolution</span>的比率縮放。 如果產生的影像大於縮圖，則會裁剪影像以符合大小；如果縮放的影像小於縮圖，則剩餘的區域會以<span class="codeph">屬性填滿：：ThumbBkgColor</span>。 <span class="codeph">屬性：：ThumbHorizAlign</span>和<span class="codeph">屬性：：ThumbVertAlign</span>是用來決定裁切矩形在較大影像中的位置，或是縮圖內較小影像的位置。 </p></td> 
 </tr> 
</table>

使用者端要求影像縮圖並顯示`req=tmb`個要求。

## 屬性 {#section-c58a8e67c2134ca3a0edd21b20dd3052}

列舉值。 有效值為1、2或3，分別對應至「裁切」、「符合」和「紋理」型別。

## 預設 {#section-a6a7c43a83384a4aab861a48d73c7c26}

如果欄位不存在、值為0或欄位為空，則會使用`attribute::ThumbType`。

## 另請參閱 {#section-fc1a79d3e6274b4381a17da159649a07}

[attribute：：ThumbType](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbtype.md#reference-329e9dbf3e5f49548d1eb61915b538f5) ， [attribute：：ThumbBkgColor](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbbkgcolor.md#reference-8e38088e79a54446a9106d0b93c9b31e)， [attribute：：ThumbHorizAlign](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbhorizalign.md#reference-0ae8b88669df4769a9053b22aca33691)， [attribute：：ThumbVertAlign](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbvertalign.md#reference-d47c6b34588c4855b04ad134e472f04f)， [catalog：：ThumbRes](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbres-cat.md#reference-eedb9991397347c3bed5bd0a785c4c69)， [catalog：：Resolution](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1)， [req=tmb](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)， [縮圖縮放](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f)
