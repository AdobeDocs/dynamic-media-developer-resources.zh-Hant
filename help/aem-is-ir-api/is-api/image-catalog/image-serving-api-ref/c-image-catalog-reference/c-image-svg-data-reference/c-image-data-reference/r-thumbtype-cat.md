---
description: 縮圖類型。 說明如何產生此影像的縮圖。
seo-description: 縮圖類型。 說明如何產生此影像的縮圖。
seo-title: ThumbType
solution: Experience Manager
title: ThumbType
uuid: b737b5a4-ad6d-4a9c-b48f-81cf170dd210
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 1%

---


# ThumbType{#thumbtype}

縮圖類型。 說明如何產生此影像的縮圖。

支援下列縮圖類型：

<table id="simpletable_874E4190A1DC4FB0AE1B2E3734746527"> 
 <tr class="strow"> 
  <td class="stentry"> <p>裁切(1) </p></td> 
  <td class="stentry"> <p>將影像裁切成縮圖外觀比例。 除非縮圖矩形和影像的長寬比完全相同，否則會裁切部分影像，以確保整個縮圖矩形都會填入影像資料。 裁切矩形是使用<span class="codeph">屬性：:ThumbHorizAlign</span>和<span class="codeph">屬性：:ThumbVertAlign</span>放在影像中。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>適合(2) </p></td> 
  <td class="stentry"> <p>將整個影像調整到縮圖矩形中。 影像會使用<span class="codeph">屬性：:ThumbHorizAlign</span>和<span class="codeph">屬性：:ThumbVertAlign</span>放置在縮圖矩形內，而任何額外的空格都會填入<span class="codeph">屬性：:ThumbBkgColor</span>。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>紋理(3) </p></td> 
  <td class="stentry"> <p>根據解析度裁切影像。 該影像按<span class="codeph">目錄：:ThumbRes</span>與<span class="codeph">目錄：:Resolution</span>的比例縮放。 如果產生的影像大於縮圖，則會裁切以符合大小，如果縮放的影像小於縮圖，則剩餘的區域會填入<span class="codeph">屬性：:ThumbBkgColor</span>。 <span class="codeph"> 屬性：::</span> ThumbHorizAlignand屬 <span class="codeph"> 性：:</span> ThumbVertAlignar用於確定裁切矩形在較大影像中的位置，或在縮圖中較小影像的位置。 </p></td> 
 </tr> 
</table>

客戶端請求具有`req=tmb`請求的影像縮圖。

## 屬性 {#section-c58a8e67c2134ca3a0edd21b20dd3052}

列舉值。 有效值為1、2或3，分別對應於「裁切」、「最適」和「紋理」類型。

## 預設 {#section-a6a7c43a83384a4aab861a48d73c7c26}

`attribute::ThumbType` 如果欄位不存在、值為0或欄位空白，則會使用。

## 另請參閱 {#section-fc1a79d3e6274b4381a17da159649a07}

[屬性：:AlignType](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbtype.md#reference-329e9dbf3e5f49548d1eb61915b538f5) ，屬性：:ThumbKgColor [，屬性：ThumbHorizColor](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbbkgcolor.md#reference-8e38088e79a54446a9106d0b93c9b31e)，屬性：ThumbHorizAttribute: [ThumbAlignAlign](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbhorizalign.md#reference-0ae8b88669df4769a9053b22aca33691) [](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbvertalign.md#reference-d47c6b34588c4855b04ad134e472f04f) [](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbres-cat.md#reference-eedb9991397347c3bed5bd0a785c4c69) [](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1) [](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76) [::AlignResShardScaling:AlignShareDCatShar：縮圖](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f)
