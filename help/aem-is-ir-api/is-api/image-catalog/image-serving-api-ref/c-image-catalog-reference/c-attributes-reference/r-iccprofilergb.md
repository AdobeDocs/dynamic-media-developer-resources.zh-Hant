---
description: RGB預設輸出色彩描述檔。 指定當未使用icc=指定輸出色域時，用於RGB響應影像的ICC顏色配置檔案的名稱，以及使用各種「影像服務」命令（如color=）指定的特定RGB顏色值。
solution: Experience Manager
title: IccProfileRgb
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 2%

---


# IccProfileRgb{#iccprofilergb}

RGB預設輸出色彩描述檔。 指定當未使用icc=指定輸出色域時，用於RGB響應影像的ICC顏色配置檔案的名稱，以及使用各種「影像服務」命令（如color=）指定的特定RGB顏色值。

## 屬性 {#section-3dd55c954d4d4ad4bb715ed7cee31025}

文字字串。 如果指定，則必須是此映像目錄或預設目錄的ICC配置檔案映射中的有效`icc::Name`值，或是相對於`attribute::RootPath`的檔案路徑。 參考的ICC描述檔必須是RGB描述檔。

## 預設 {#section-dfe08dd7b851453ca816623a4179955b}

如果未定義或為空，則繼承自`default::IccProfileRgb`。

## 另請參閱 {#section-05bc25ab7caa418ca94d43ced905add7}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) ，屬 [性：:IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f)，屬 [性：:IccProfileSrcRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcrgb.md#reference-b8e576d075b44f5c94d95bfb5aa22ae2), [屬性：:RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
