---
description: RGB預設輸出顏色配置檔案。 指定在未使用icc=指定輸出顏色空間時用於RGB響應影像的ICC顏色配置檔案的名稱，以及使用各種「影像服務」命令（如color=）指定的某些RGB顏色值。
solution: Experience Manager
title: IccProfileRgb
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 861c7b54-6d18-47c8-a08d-970f29b63962
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 2%

---

# IccProfileRgb{#iccprofilergb}

RGB預設輸出顏色配置檔案。 指定在未使用icc=指定輸出顏色空間時用於RGB響應影像的ICC顏色配置檔案的名稱，以及使用各種「影像服務」命令（如color=）指定的某些RGB顏色值。

## 屬性 {#section-3dd55c954d4d4ad4bb715ed7cee31025}

文本字串。 如果指定，則必須是有效 `icc::Name` 此影像目錄或預設目錄或相對於 `attribute::RootPath`。 引用的ICC配置檔案必須是RGB配置檔案。

## 預設 {#section-dfe08dd7b851453ca816623a4179955b}

繼承自 `default::IccProfileRgb` 或為空。

## 另請參閱 {#section-05bc25ab7caa418ca94d43ced905add7}

[icc:：名稱](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) 。 [屬性：:IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f)。 [屬性：:IccProfileSrcRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcrgb.md#reference-b8e576d075b44f5c94d95bfb5aa22ae2)。 [屬性：:RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
