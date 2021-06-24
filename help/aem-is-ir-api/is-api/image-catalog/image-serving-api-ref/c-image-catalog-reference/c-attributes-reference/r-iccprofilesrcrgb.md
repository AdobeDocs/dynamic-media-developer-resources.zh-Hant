---
description: RGB預設輸入顏色配置檔案。 指定用於未嵌入顏色配置檔案的RGB源影像的ICC顏色配置檔案的名稱，以及用各種「影像伺服」命令（如color=）指定的某些RGB顏色值的名稱。
solution: Experience Manager
title: IccProfileSrcRgb
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: dfcbd9fe-e696-46e3-abbf-497dc55fe855
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 2%

---

# IccProfileSrcRgb{#iccprofilesrcrgb}

RGB預設輸入顏色配置檔案。 指定用於未嵌入顏色配置檔案的RGB源影像的ICC顏色配置檔案的名稱，以及用各種「影像伺服」命令（如color=）指定的某些RGB顏色值的名稱。

## 屬性 {#section-3cd753196959462e9e674dab0b033d08}

文字字串。 如果指定，則必須是此影像目錄或預設目錄的ICC配置檔案映射中的有效`icc::Name`值，或相對於`attribute::RootPath`的檔案路徑。 引用的ICC配置檔案必須是RGB配置檔案。

## 預設 {#section-2c3cb2d9c9bf4aa7896e51b5d444ddee}

如果未定義或為空，則從`default::IccProfileSrcRgb`繼承。 如果`attribute::IccProfileSrcRgb`未解析為有效的設定檔，則會改用`attribute::IccProfileRgb`。

## 另請參閱 {#section-d6e5c6eeaea4445ba7fb5737cd193a48}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) , [屬性：:IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [屬性：:IccProfileRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilergb.md#reference-3479e7daac54404f84b06b98ca07b9df), [屬性：:RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
