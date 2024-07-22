---
title: IccProfileGray
description: 灰階預設輸出色彩設定檔。 指定當icc=未指定輸出色域時，用於灰階回應影像的ICC色彩設定檔名稱，以及指定各種「影像伺服」命令（例如color=）的特定灰階色彩值。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4964c3b3-799d-40cb-bc5f-d08acfd41ed9
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 2%

---

# IccProfileGray{#iccprofilegray}

灰階預設輸出色彩設定檔。 指定當icc=未指定輸出色域時，用於灰階回應影像的ICC色彩設定檔名稱，以及指定各種「影像伺服」命令（例如color=）的特定灰階色彩值。

## 屬性 {#section-03f090ee2acf4537b83f78840d23ecab}

文字字串。 如果已指定，則必須是來自此影像目錄或預設目錄之ICC設定檔對映的有效`icc::Name`值，或是相對於`attribute::RootPath`的檔案路徑。 參照的ICC設定檔必須是灰階設定檔。

## 預設 {#section-95ba3ab15edc4259b657c6ebf8783d61}

如果未定義或空白，則繼承自`default::IccProfileGray`。

## 另請參閱 {#section-b737b9a6a8bd4997b660292301ba967b}

[icc：：Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) ， [attribute：：IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f)， [attribute：：IccProfileSrcGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9)， [attribute：：RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
