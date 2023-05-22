---
description: CMYK預設輸出顏色配置檔案。 指定在未使用icc=指定輸出顏色空間時用於CMYK響應影像的ICC顏色配置檔案的名稱，以及使用各種「影像服務」命令（如color=）指定的某些CMYK顏色值的名稱。
solution: Experience Manager
title: IccProfileCmyk
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2bf83cf5-3fc9-42aa-a143-4b56e43ee4d1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 2%

---

# IccProfileCmyk{#iccprofilecmyk}

CMYK預設輸出顏色配置檔案。 指定在未使用icc=指定輸出顏色空間時用於CMYK響應影像的ICC顏色配置檔案的名稱，以及使用各種「影像服務」命令（如color=）指定的某些CMYK顏色值的名稱。

## 屬性 {#section-d8b6102cc1c744d482f99808ccfcaa24}

文本字串。 如果指定，則必須是有效 `icc::Name` 此影像目錄或預設目錄或相對於 `attribute::RootPath`。 引用的ICC配置檔案必須是CMYK配置檔案。

## 預設 {#section-62442df09a724950bfbdd0640b3e6678}

繼承自 `default::IccProfileCmyk` 或為空。

## 另請參閱 {#section-17071d1ed5ad469490fd715ba8f4d30d}

[icc:：名稱](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) 。 [屬性：:IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f)。 [屬性：:IccProfileSrcCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrccmyk.md#reference-b57196dfe5db41fe88bd0828ed4ec728)。 [屬性：:RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
