---
description: RGB預設輸入色彩設定檔。 指定用於RGB來源影像（未嵌入色彩設定檔）的ICC色彩設定檔名稱，以及用於使用各種「影像伺服」命令（例如color=）指定的某些RGB色彩值。
solution: Experience Manager
title: IccProfileSrcRgb
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dfcbd9fe-e696-46e3-abbf-497dc55fe855
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 1%

---

# IccProfileSrcRgb{#iccprofilesrcrgb}

RGB預設輸入色彩設定檔。 指定用於RGB來源影像（未嵌入色彩設定檔）的ICC色彩設定檔名稱，以及用於使用各種「影像伺服」命令（例如color=）指定的某些RGB色彩值。

## 屬性 {#section-3cd753196959462e9e674dab0b033d08}

文字字串。 如果已指定，則必須是來自此影像目錄或預設目錄之ICC設定檔對映的有效`icc::Name`值，或是相對於`attribute::RootPath`的檔案路徑。 參考的ICC設定檔必須是RGB設定檔。

## 預設 {#section-2c3cb2d9c9bf4aa7896e51b5d444ddee}

如果未定義或空白，則繼承自`default::IccProfileSrcRgb`。 如果`attribute::IccProfileSrcRgb`未解析為有效的設定檔，則改用`attribute::IccProfileRgb`。

## 另請參閱 {#section-d6e5c6eeaea4445ba7fb5737cd193a48}

[icc：：Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) ，[attribute：：IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f)，[attribute：：IccProfileRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilergb.md#reference-3479e7daac54404f84b06b98ca07b9df)，[attribute：：RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
