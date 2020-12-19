---
description: 縮圖的垂直對齊。 指定由wid=和hei=或由屬性DefaultThumbPix指定的回覆影像矩形中縮圖影像的垂直對齊方式。
seo-description: 縮圖的垂直對齊。 指定由wid=和hei=或由屬性DefaultThumbPix指定的回覆影像矩形中縮圖影像的垂直對齊方式。
seo-title: ThumbVertAlign
solution: Experience Manager
title: ThumbVertAlign
topic: Scene7 Image Serving - Image Rendering API
uuid: a90281eb-9681-4b4a-a94b-663f007fb32f
translation-type: tm+mt
source-git-commit: b4331c6f033903ec64f168da0b739927c6066710
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 3%

---


# ThumbVertAlign{#thumbvertalign}

縮圖的垂直對齊。 指定由wid=和hei=或attribute::DefaultThumbPix指定的回覆影像矩形中縮圖影像的垂直對齊方式。

僅用於縮圖請求(`req=tmb`)。

## 屬性 {#section-f02c23248e87419caf3d95add51aea1e}

列舉。 上、中和下對齊的允許值分別為1、2和3。

## 預設 {#section-30caa4e772254419ad7a3a89d440666c}

如果未定義或為空，則繼承自`default::ThumbHorizAlign`。

## 另請參閱 {#section-c4cd5209d994498eb56a78fcd5bbdfa4}

[catalog:::ThumbType](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbtype-cat.md) ,  [attribute::DefaultThumbPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultthumbpix.md#reference-cf52bb74bed2466e8bc8adb0cacd6141),  [wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47), [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)
