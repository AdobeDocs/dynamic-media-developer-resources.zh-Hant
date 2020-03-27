---
description: 灰階預設輸入色彩描述檔。 指定不嵌入色彩描述檔的灰階來源影像，以及使用各種「影像伺服」指令（例如color=）指定的特定灰階色彩值，所使用之ICC色彩描述檔的名稱。
seo-description: 灰階預設輸入色彩描述檔。 指定不嵌入色彩描述檔的灰階來源影像，以及使用各種「影像伺服」指令（例如color=）指定的特定灰階色彩值，所使用之ICC色彩描述檔的名稱。
seo-title: IccProfileSrcGray
solution: Experience Manager
title: IccProfileSrcGray
topic: Scene7 Image Serving - Image Rendering API
uuid: 823c0e33-8bb7-4754-81cf-61a5ed6f45ce
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# IccProfileSrcGray{#iccprofilesrcgray}

灰階預設輸入色彩描述檔。 指定不嵌入色彩描述檔的灰階來源影像，以及使用各種「影像伺服」指令（例如color=）指定的特定灰階色彩值，所使用之ICC色彩描述檔的名稱。

## 屬性 {#section-8cbb316df6eb463aaca7b308d3568086}

文字字串。 如果指定，則必須是此映 `icc::Name` 像目錄或預設目錄的ICC配置檔案映射中的有效值，或相對於的檔案路徑 `attribute::RootPath`。 參考的ICC配置檔案必須是灰度配置檔案。

## 預設 {#section-bcc7250715884412bd0780f60d1cce7b}

繼承自 `default::IccProfileSrcGray` （如果未定義或為空）。 如果 `attribute::IccProfileSrcGray` 未解析為有效的描述檔，則 `attribute::IccProfileGray` 會改用。

## 另請參閱 {#section-e429b76daf2e4b92b326db2b0bcbd0c5}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) , [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [attribute::IccProfileGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilegray.md#reference-13822a1596e440eea0492e86d88dad35), [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
