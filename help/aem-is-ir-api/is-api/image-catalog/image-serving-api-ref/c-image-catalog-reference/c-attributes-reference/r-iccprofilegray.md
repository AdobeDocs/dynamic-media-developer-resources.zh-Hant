---
description: 灰階預設輸出色彩描述檔。 指定當未使用icc=指定輸出色域時，用於灰階響應影像的ICC顏色配置檔案的名稱，以及使用各種「影像服務」命令（如color=）指定的某些灰階顏色值。
seo-description: 灰階預設輸出色彩描述檔。 指定當未使用icc=指定輸出色域時，用於灰階響應影像的ICC顏色配置檔案的名稱，以及使用各種「影像服務」命令（如color=）指定的某些灰階顏色值。
seo-title: IccProfileGray
solution: Experience Manager
title: IccProfileGray
topic: Scene7 Image Serving - Image Rendering API
uuid: a7d40114-f91f-4637-bb49-5b06b9ce846d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# IccProfileGray{#iccprofilegray}

灰階預設輸出色彩描述檔。 指定當未使用icc=指定輸出色域時，用於灰階響應影像的ICC顏色配置檔案的名稱，以及使用各種「影像服務」命令（如color=）指定的某些灰階顏色值。

## 屬性 {#section-03f090ee2acf4537b83f78840d23ecab}

文字字串。 如果指定，則必須是此映 `icc::Name` 像目錄或預設目錄的ICC配置檔案映射中的有效值，或相對於的檔案路徑 `attribute::RootPath`。 參考的ICC配置檔案必須是灰度配置檔案。

## 預設 {#section-95ba3ab15edc4259b657c6ebf8783d61}

繼承自 `default::IccProfileGray` （如果未定義或為空）。

## 另請參閱 {#section-b737b9a6a8bd4997b660292301ba967b}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) ，屬 [性：:IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f)，屬 [性：:IccProfileSrcGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9), [屬性：:RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
