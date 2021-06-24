---
description: CMYK預設輸入顏色配置檔案。 指定用於未嵌入顏色配置檔案的CMYK源影像的ICC顏色配置檔案的名稱，以及用各種「影像伺服」命令（如color=）指定的某些CMYK顏色值的名稱。
solution: Experience Manager
title: IccProfileSrcCmyk
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 018170f3-2d1a-4da1-a480-b0a7e19457d8
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 2%

---

# IccProfileSrcCmyk{#iccprofilesrccmyk}

CMYK預設輸入顏色配置檔案。 指定用於未嵌入顏色配置檔案的CMYK源影像的ICC顏色配置檔案的名稱，以及用各種「影像伺服」命令（如color=）指定的某些CMYK顏色值的名稱。

## 屬性 {#section-fc2ad12a3c6e4c7cab495f1878638e66}

文字字串。 如果指定，則必須是此影像目錄或預設目錄的ICC配置檔案映射中的有效`icc::Name`值，或相對於`attribute::RootPath`的檔案路徑。 引用的ICC配置檔案必須是CMYK配置檔案。

## 預設 {#section-c1f63b4bd32a4f38bf5d68decb9e25da}

如果未定義或為空，則從`default::IccProfileSrcCmyk`繼承。 如果`attribute::IccProfileSrcCmyk`未解析為有效的設定檔，則會改用`attribute::IccProfileCmyk`。

## 另請參閱 {#section-a6623bd4277e43b084ec0fb9e02069dc}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) , [屬性：:IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [屬性：:IccProfileCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0), [屬性：:RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
