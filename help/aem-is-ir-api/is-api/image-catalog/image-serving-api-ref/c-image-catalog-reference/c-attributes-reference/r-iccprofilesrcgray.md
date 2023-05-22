---
description: 灰度預設輸入顏色配置檔案。 指定ICC顏色配置檔案的名稱，該ICC顏色配置檔案用於不嵌入顏色配置檔案的灰度源影像以及使用各種「影像服務」命令（如color=）指定的某些灰度顏色值。
solution: Experience Manager
title: IccProfileSrcGray
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 54290f71-36b2-4b37-ac04-4fe85c1f34ab
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 1%

---

# IccProfileSrcGray{#iccprofilesrcgray}

灰度預設輸入顏色配置檔案。 指定ICC顏色配置檔案的名稱，該ICC顏色配置檔案用於不嵌入顏色配置檔案的灰度源影像以及使用各種「影像服務」命令（如color=）指定的某些灰度顏色值。

## 屬性 {#section-8cbb316df6eb463aaca7b308d3568086}

文本字串。 如果指定，則必須是有效 `icc::Name` 此影像目錄或預設目錄或相對於 `attribute::RootPath`。 引用的ICC配置檔案必須是灰度配置檔案。

## 預設 {#section-bcc7250715884412bd0780f60d1cce7b}

繼承自 `default::IccProfileSrcGray` 或為空。 如果 `attribute::IccProfileSrcGray` 未解析為有效的配置檔案， `attribute::IccProfileGray` 的雙曲餘切值。

## 另請參閱 {#section-e429b76daf2e4b92b326db2b0bcbd0c5}

[icc:：名稱](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) 。 [屬性：:IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f)。 [屬性：:IccProfileGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilegray.md#reference-13822a1596e440eea0492e86d88dad35)。 [屬性：:RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
