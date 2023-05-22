---
title: IccProfileSrcCmyk
description: CMYK預設輸入顏色配置檔案。 指定CMYK顏色配置檔案的名稱，用於不嵌入顏色配置檔案的CMYK源影像，以及使用各種「影像服務」命令（如color=）指定的某些CMYK顏色值。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 018170f3-2d1a-4da1-a480-b0a7e19457d8
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 1%

---

# IccProfileSrcCmyk{#iccprofilesrccmyk}

CMYK預設輸入顏色配置檔案。 指定CMYK顏色配置檔案的名稱，用於不嵌入顏色配置檔案的CMYK源影像，以及使用各種「影像服務」命令（如color=）指定的某些CMYK顏色值。

## 屬性 {#section-fc2ad12a3c6e4c7cab495f1878638e66}

文本字串。 如果指定，則必須是有效 `icc::Name` 此影像目錄或預設目錄或相對於 `attribute::RootPath`。 引用的ICC配置檔案必須是CMYK配置檔案。

## 預設 {#section-c1f63b4bd32a4f38bf5d68decb9e25da}

繼承自 `default::IccProfileSrcCmyk` 或為空。 如果 `attribute::IccProfileSrcCmyk` 未解析為有效的配置檔案， `attribute::IccProfileCmyk` 的雙曲餘切值。

## 另請參閱 {#section-a6623bd4277e43b084ec0fb9e02069dc}

[icc:：名稱](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) 。 [屬性：:IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f)。 [屬性：:IccProfileCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0)。 [屬性：:RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
