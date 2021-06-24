---
description: RGB預設輸出顏色配置檔案。 指定當未使用icc=指定輸出顏色空間時，用於RGB響應影像的ICC顏色配置檔案的名稱，以及用各種「影像伺服」命令（如color=）指定的某些RGB顏色值。
solution: Experience Manager
title: IccProfileRgb
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 861c7b54-6d18-47c8-a08d-970f29b63962
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 2%

---

# IccProfileRgb{#iccprofilergb}

RGB預設輸出顏色配置檔案。 指定當未使用icc=指定輸出顏色空間時，用於RGB響應影像的ICC顏色配置檔案的名稱，以及用各種「影像伺服」命令（如color=）指定的某些RGB顏色值。

## 屬性 {#section-3dd55c954d4d4ad4bb715ed7cee31025}

文字字串。 如果指定，則必須是此影像目錄或預設目錄的ICC配置檔案映射中的有效`icc::Name`值，或相對於`attribute::RootPath`的檔案路徑。 引用的ICC配置檔案必須是RGB配置檔案。

## 預設 {#section-dfe08dd7b851453ca816623a4179955b}

如果未定義或為空，則從`default::IccProfileRgb`繼承。

## 另請參閱 {#section-05bc25ab7caa418ca94d43ced905add7}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) ,  [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f)，屬性：:IccProfileSrcRgb [, ](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcrgb.md#reference-b8e576d075b44f5c94d95bfb5aa22ae2) [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
