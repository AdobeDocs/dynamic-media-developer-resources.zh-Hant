---
description: CMYK預設輸出色彩描述檔。 指定當未使用icc=指定輸出色域時，用於CMYK響應影像的ICC顏色配置檔案的名稱，以及使用各種「影像服務」命令（如color=）指定的特定CMYK顏色值的名稱。
solution: Experience Manager
title: IccProfileCmyk
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 2%

---


# IccProfileCmyk{#iccprofilecmyk}

CMYK預設輸出色彩描述檔。 指定當未使用icc=指定輸出色域時，用於CMYK響應影像的ICC顏色配置檔案的名稱，以及使用各種「影像服務」命令（如color=）指定的特定CMYK顏色值的名稱。

## 屬性 {#section-d8b6102cc1c744d482f99808ccfcaa24}

文字字串。 如果指定，則必須是此映像目錄或預設目錄的ICC配置檔案映射中的有效`icc::Name`值，或是相對於`attribute::RootPath`的檔案路徑。 參考的ICC描述檔必須是CMYK描述檔。

## 預設 {#section-62442df09a724950bfbdd0640b3e6678}

如果未定義或為空，則繼承自`default::IccProfileCmyk`。

## 另請參閱 {#section-17071d1ed5ad469490fd715ba8f4d30d}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) ，屬 [性：:IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f)，屬 [性：:IccProfileSrcCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrccmyk.md#reference-b57196dfe5db41fe88bd0828ed4ec728), [屬性：:RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
