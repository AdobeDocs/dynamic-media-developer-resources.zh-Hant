---
description: 縮圖類型。 說明如何產生此影像的縮圖。
seo-description: 縮圖類型。 說明如何產生此影像的縮圖。
seo-title: ThumbType
solution: Experience Manager
title: ThumbType
topic: Scene7 Image Serving - Image Rendering API
uuid: b737b5a4-ad6d-4a9c-b48f-81cf170dd210
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ThumbType{#thumbtype}

縮圖類型。 說明如何產生此影像的縮圖。

支援下列縮圖類型：

<table id="simpletable_874E4190A1DC4FB0AE1B2E3734746527"> 
 <tr class="strow"> 
  <td class="stentry"> <p>裁切(1) </p></td> 
  <td class="stentry"> <p>將影像裁切成縮圖外觀比例。 除非縮圖矩形和影像的長寬比完全相同，否則會裁切部分影像，以確保整個縮圖矩形都會填入影像資料。 裁切矩形會使用屬性：:ThumbHorizAlign <span class="codeph"> 和屬性</span> : <span class="codeph"> :ThumbVertAlign放在影像中</span>。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>適合(2) </p></td> 
  <td class="stentry"> <p>將整個影像調整到縮圖矩形中。 影像會使用屬性：:ThumbHorizAlign <span class="codeph"> and</span> attribute::ThumbVertAlign <span class="codeph"> ，而任何額外的空格都會填入屬性：:ThumbBkgColor</span><span class="codeph"></span>。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>紋理(3) </p></td> 
  <td class="stentry"> <p>根據解析度裁切影像。 影像會依目錄：:ThumbRes <span class="codeph"> 與目錄</span> : <span class="codeph"> :Resolution的比例縮放</span>。 如果產生的影像大於縮圖，則會裁切以符合大小，如果縮放的影像小於縮圖，則剩餘的區域會填入 <span class="codeph"> 屬性：:ThumbBkgColor</span>。 <span class="codeph"> 屬性：::ThumbHorizAlign</span> and <span class="codeph"> attribute::ThumbVertAlign</span> ，用於確定裁切矩形在較大影像中的位置，或縮圖中較小影像的位置。 </p></td> 
 </tr> 
</table>

用戶端會隨請求要求影像縮 `req=tmb` 圖。

## 屬性 {#section-c58a8e67c2134ca3a0edd21b20dd3052}

列舉值。 有效值為1、2或3，分別對應於「裁切」、「最適」和「紋理」類型。

## 預設 {#section-a6a7c43a83384a4aab861a48d73c7c26}

`attribute::ThumbType` 如果欄位不存在、值為0或欄位空白，則會使用。

## 另請參閱 {#section-fc1a79d3e6274b4381a17da159649a07}

[屬性：:ThumbType](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbtype.md#reference-329e9dbf3e5f49548d1eb61915b538f5) ，屬性：:ThumbKgColor [，屬性：ThumbHorizColor](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbbkgcolor.md#reference-8e38088e79a54446a9106d0b93c9b31e)，屬性：ThumbHorizAttribute: [ThumbAlignAlign](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbhorizalign.md#reference-0ae8b88669df4769a9053b22aca33691)[](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbvertalign.md#reference-d47c6b34588c4855b04ad134e472f04f)[](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbres-cat.md#reference-eedb9991397347c3bed5bd0a785c4c69)[](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1)[](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)[::AlignResShard:AlignScalignShare:Dit,CalatDCatDCatal:](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f)
