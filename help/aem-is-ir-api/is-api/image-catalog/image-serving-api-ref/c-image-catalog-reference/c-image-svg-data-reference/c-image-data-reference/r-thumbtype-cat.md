---
description: 縮略圖類型。 描述如何生成此影像的縮略圖。
solution: Experience Manager
title: ThumbType
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a90b587d-6893-44e4-8dce-7676bc7eebe3
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 1%

---

# ThumbType{#thumbtype}

縮略圖類型。 描述如何生成此影像的縮略圖。

支援以下縮略圖類型：

<table id="simpletable_874E4190A1DC4FB0AE1B2E3734746527"> 
 <tr class="strow"> 
  <td class="stentry"> <p>裁剪(1) </p></td> 
  <td class="stentry"> <p>將影像裁剪到縮略圖縱橫比。 除非縮略圖矩形和影像的長寬比完全相同，否則影像的一部分會被剪切以確保整個縮略圖矩形都填充有影像資料。 裁剪矩形位於影像中，使用 <span class="codeph"> 屬性：:ThumbHorizAlign</span> 和 <span class="codeph"> 屬性：:ThumbVertAlign</span>。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>適合(2) </p></td> 
  <td class="stentry"> <p>將整個影像調整到縮略圖矩形中。 影像位於縮覽圖矩形內，使用 <span class="codeph"> 屬性：:ThumbHorizAlign</span> 和 <span class="codeph"> 屬性：:ThumbVertAlign</span>，並且任何額外的空間 <span class="codeph"> 屬性：:ThumbBkgColor</span>。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>紋理(3) </p></td> 
  <td class="stentry"> <p>根據解析度裁剪影像。 影像按 <span class="codeph"> 目錄：:ThumbRes</span> 至 <span class="codeph"> 目錄：：解析</span>。 如果生成的影像大於縮略圖，則會裁切該影像以適合；如果縮放的影像小於縮略圖，則剩餘區域將填充 <span class="codeph"> 屬性：:ThumbBkgColor</span>。 <span class="codeph"> 屬性：:ThumbHorizAlign</span> 和 <span class="codeph"> 屬性：:ThumbVertAlign</span> 用於確定裁剪矩形在較大影像中的位置或較小影像在縮略圖中的位置。 </p></td> 
 </tr> 
</table>

客戶端請求影像縮略圖 `req=tmb` 請求。

## 屬性 {#section-c58a8e67c2134ca3a0edd21b20dd3052}

枚舉值。 有效值為1、2或3，它們分別對應於「裁剪」、「擬合」和「紋理」類型。

## 預設 {#section-a6a7c43a83384a4aab861a48d73c7c26}

`attribute::ThumbType` 如果欄位不存在，則使用。

## 另請參閱 {#section-fc1a79d3e6274b4381a17da159649a07}

[屬性：:ThumbType](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbtype.md#reference-329e9dbf3e5f49548d1eb61915b538f5) 。 [屬性：:ThumbBkgColor](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbbkgcolor.md#reference-8e38088e79a54446a9106d0b93c9b31e)。 [屬性：:ThumbHorizAlign](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbhorizalign.md#reference-0ae8b88669df4769a9053b22aca33691)。 [屬性：:ThumbVertAlign](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbvertalign.md#reference-d47c6b34588c4855b04ad134e472f04f)。 [目錄：:ThumbRes](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbres-cat.md#reference-eedb9991397347c3bed5bd0a785c4c69)。 [目錄：：解析](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1)。 [req=tmb](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)。 [縮略圖縮放](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f)
