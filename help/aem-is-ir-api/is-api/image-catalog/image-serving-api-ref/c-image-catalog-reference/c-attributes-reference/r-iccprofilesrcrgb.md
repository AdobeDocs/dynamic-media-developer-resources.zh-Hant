---
description: RGB預設輸入色彩描述檔。 指定不嵌入色彩描述檔的RGB來源影像，以及使用各種「影像伺服」指令（例如color=）指定的特定RGB色彩值，所使用之ICC色彩描述檔的名稱。
seo-description: RGB預設輸入色彩描述檔。 指定不嵌入色彩描述檔的RGB來源影像，以及使用各種「影像伺服」指令（例如color=）指定的特定RGB色彩值，所使用之ICC色彩描述檔的名稱。
seo-title: IccProfileSrcRgb
solution: Experience Manager
title: IccProfileSrcRgb
uuid: 4f6f19ec-3524-403e-9c79-1e2b25cd74ce
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 1%

---


# IccProfileSrcRgb{#iccprofilesrcrgb}

RGB預設輸入色彩描述檔。 指定不嵌入色彩描述檔的RGB來源影像，以及使用各種「影像伺服」指令（例如color=）指定的特定RGB色彩值，所使用之ICC色彩描述檔的名稱。

## 屬性 {#section-3cd753196959462e9e674dab0b033d08}

文字字串。 如果指定，則必須是此映像目錄或預設目錄的ICC配置檔案映射中的有效`icc::Name`值，或是相對於`attribute::RootPath`的檔案路徑。 參考的ICC描述檔必須是RGB描述檔。

## 預設 {#section-2c3cb2d9c9bf4aa7896e51b5d444ddee}

如果未定義或為空，則繼承自`default::IccProfileSrcRgb`。 如果`attribute::IccProfileSrcRgb`未解析為有效的配置式，則改用`attribute::IccProfileRgb`。

## 另請參閱 {#section-d6e5c6eeaea4445ba7fb5737cd193a48}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) ,  [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f),  [attribute::IccProfileRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilergb.md#reference-3479e7daac54404f84b06b98ca07b9df),  [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
