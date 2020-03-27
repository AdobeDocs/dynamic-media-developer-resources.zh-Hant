---
description: RGB預設輸入色彩描述檔。 指定不嵌入色彩描述檔的RGB來源影像，以及使用各種「影像伺服」指令（例如color=）指定的特定RGB色彩值，所使用之ICC色彩描述檔的名稱。
seo-description: RGB預設輸入色彩描述檔。 指定不嵌入色彩描述檔的RGB來源影像，以及使用各種「影像伺服」指令（例如color=）指定的特定RGB色彩值，所使用之ICC色彩描述檔的名稱。
seo-title: IccProfileSrcRgb
solution: Experience Manager
title: IccProfileSrcRgb
topic: Scene7 Image Serving - Image Rendering API
uuid: 4f6f19ec-3524-403e-9c79-1e2b25cd74ce
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# IccProfileSrcRgb{#iccprofilesrcrgb}

RGB預設輸入色彩描述檔。 指定不嵌入色彩描述檔的RGB來源影像，以及使用各種「影像伺服」指令（例如color=）指定的特定RGB色彩值，所使用之ICC色彩描述檔的名稱。

## 屬性 {#section-3cd753196959462e9e674dab0b033d08}

文字字串。 如果指定，則必須是此映 `icc::Name` 像目錄或預設目錄的ICC配置檔案映射中的有效值，或相對於的檔案路徑 `attribute::RootPath`。 參考的ICC描述檔必須是RGB描述檔。

## 預設 {#section-2c3cb2d9c9bf4aa7896e51b5d444ddee}

繼承自 `default::IccProfileSrcRgb` （如果未定義或為空）。 如果 `attribute::IccProfileSrcRgb` 未解析為有效的描述檔，則 `attribute::IccProfileRgb` 會改用。

## 另請參閱 {#section-d6e5c6eeaea4445ba7fb5737cd193a48}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) , [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [attribute::IccProfileRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilergb.md#reference-3479e7daac54404f84b06b98ca07b9df), [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
