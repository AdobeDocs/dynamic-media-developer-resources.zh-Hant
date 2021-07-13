---
description: 縮圖的垂直對齊方式。 在由wid=和hei=或屬性DefaultThumbPix指定的回復影像矩形中指定縮略圖影像的垂直對齊方式。
solution: Experience Manager
title: ThumbVertAlign
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: bb1aa398-5638-4109-bf05-bc51ace4146d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 4%

---

# ThumbVertAlign{#thumbvertalign}

縮圖的垂直對齊方式。 在由wid=和hei=或屬性：:DefaultThumbPix指定的回復影像矩形中指定縮略圖影像的垂直對齊方式。

僅用於縮圖請求(`req=tmb`)。

## 屬性 {#section-f02c23248e87419caf3d95add51aea1e}

列舉。 頂部對齊、中心對齊和底部對齊的允許值分別為1、2和3。

## 預設 {#section-30caa4e772254419ad7a3a89d440666c}

如果未定義或為空，則從`default::ThumbHorizAlign`繼承。

## 另請參閱 {#section-c4cd5209d994498eb56a78fcd5bbdfa4}

[catalog::ThumbType](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbtype-cat.md) ,  [attribute::DefaultThumbPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultthumbpix.md#reference-cf52bb74bed2466e8bc8adb0cacd6141),  [wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47),  [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)
