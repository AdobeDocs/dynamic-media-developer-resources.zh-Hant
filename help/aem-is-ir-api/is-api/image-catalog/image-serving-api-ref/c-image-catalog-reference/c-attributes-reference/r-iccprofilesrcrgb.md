---
description: RGB預設輸入顏色配置檔案。 指定ICC顏色配置檔案的名稱，該ICC顏色配置檔案用於RGB不嵌入顏色配置檔案的源影像以及使用各種「影像服務」命令指定的特定RGB顏色值，如color=。
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

RGB預設輸入顏色配置檔案。 指定ICC顏色配置檔案的名稱，該ICC顏色配置檔案用於RGB不嵌入顏色配置檔案的源影像以及使用各種「影像服務」命令指定的特定RGB顏色值，如color=。

## 屬性 {#section-3cd753196959462e9e674dab0b033d08}

文本字串。 如果指定，則必須是有效 `icc::Name` 此影像目錄或預設目錄或相對於 `attribute::RootPath`。 引用的ICC配置檔案必須是RGB配置檔案。

## 預設 {#section-2c3cb2d9c9bf4aa7896e51b5d444ddee}

繼承自 `default::IccProfileSrcRgb` 或為空。 如果 `attribute::IccProfileSrcRgb` 未解析為有效的配置檔案， `attribute::IccProfileRgb` 的雙曲餘切值。

## 另請參閱 {#section-d6e5c6eeaea4445ba7fb5737cd193a48}

[icc:：名稱](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) 。 [屬性：:IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f)。 [屬性：:IccProfileRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilergb.md#reference-3479e7daac54404f84b06b98ca07b9df)。 [屬性：:RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
