---
description: 縮圖的水準對齊。 指定由wid=和hei=或由屬性DefaultThumbPix指定的回覆影像矩形中縮圖影像的水準對齊方式。
solution: Experience Manager
title: ThumbHorizAlign
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 4%

---


# ThumbHorizAlign{#thumbhorizalign}

縮圖的水準對齊。 指定由wid=和hei=或attribute::DefaultThumbPix指定的回覆影像矩形中縮圖影像的水準對齊方式。

僅用於縮圖請求(`req=tmb`)。

## 屬性 {#section-c98f793986cd4f98a3995615e3b68f76}

列舉。 允許的值分別為1、2和3，對於左對齊、中對齊和右對齊。

## 預設 {#section-0c06f0d998cb4306868b360a06c32e5b}

如果未定義或為空，則繼承自`default::ThumbHorizAlign`。

## 另請參閱 {#section-a74a13c3643140cf971d7a4275e0fdb3}

[catalog:::ThumbType](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbtype-cat.md#reference-41149ddffc8749cba2f8d9c8e2611e03) ,  [attribute::DefaultThumbPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultthumbpix.md#reference-cf52bb74bed2466e8bc8adb0cacd6141),  [wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47), [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)
