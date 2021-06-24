---
description: 灰度預設輸入顏色配置檔案。 指定用於未嵌入顏色配置檔案的灰度源影像以及使用各種「影像服務」命令（如color=）指定的某些灰度顏色值的ICC顏色配置檔案的名稱。
solution: Experience Manager
title: IccProfileSrcGray
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 54290f71-36b2-4b37-ac04-4fe85c1f34ab
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 2%

---

# IccProfileSrcGray{#iccprofilesrcgray}

灰度預設輸入顏色配置檔案。 指定用於未嵌入顏色配置檔案的灰度源影像以及使用各種「影像服務」命令（如color=）指定的某些灰度顏色值的ICC顏色配置檔案的名稱。

## 屬性 {#section-8cbb316df6eb463aaca7b308d3568086}

文字字串。 如果指定，則必須是此影像目錄或預設目錄的ICC配置檔案映射中的有效`icc::Name`值，或相對於`attribute::RootPath`的檔案路徑。 引用的ICC配置檔案必須是灰度配置檔案。

## 預設 {#section-bcc7250715884412bd0780f60d1cce7b}

如果未定義或為空，則從`default::IccProfileSrcGray`繼承。 如果`attribute::IccProfileSrcGray`未解析為有效的設定檔，則會改用`attribute::IccProfileGray`。

## 另請參閱 {#section-e429b76daf2e4b92b326db2b0bcbd0c5}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) ,  [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f),  [attribute::IccProfileGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilegray.md#reference-13822a1596e440eea0492e86d88dad35),  [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
