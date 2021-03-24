---
description: CMYK預設輸入色彩描述檔。 指定不嵌入色彩描述檔的CMYK來源影像，以及使用各種「影像伺服」指令（例如color=）指定的特定CMYK色彩值，所要使用的ICC色彩描述檔名稱。
solution: Experience Manager
title: IccProfileSrcCmyk
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 2%

---


# IccProfileSrcCmyk{#iccprofilesrccmyk}

CMYK預設輸入色彩描述檔。 指定不嵌入色彩描述檔的CMYK來源影像，以及使用各種「影像伺服」指令（例如color=）指定的特定CMYK色彩值，所要使用的ICC色彩描述檔名稱。

## 屬性 {#section-fc2ad12a3c6e4c7cab495f1878638e66}

文字字串。 如果指定，則必須是此映像目錄或預設目錄的ICC配置檔案映射中的有效`icc::Name`值，或是相對於`attribute::RootPath`的檔案路徑。 參考的ICC描述檔必須是CMYK描述檔。

## 預設 {#section-c1f63b4bd32a4f38bf5d68decb9e25da}

如果未定義或為空，則繼承自`default::IccProfileSrcCmyk`。 如果`attribute::IccProfileSrcCmyk`未解析為有效的配置式，則改用`attribute::IccProfileCmyk`。

## 另請參閱 {#section-a6623bd4277e43b084ec0fb9e02069dc}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) ，屬 [性：:IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f)，屬 [性：:IccProfileCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0), [屬性：:RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
