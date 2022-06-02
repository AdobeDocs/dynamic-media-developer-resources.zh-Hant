---
title: Icc配置檔案灰色
description: 灰度預設輸出顏色配置檔案。 指定當未使用icc=指定輸出顏色空間時用於灰度響應影像的ICC顏色配置檔案的名稱，以及使用各種「影像服務」命令（如color=）指定的某些灰度顏色值的名稱。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4964c3b3-799d-40cb-bc5f-d08acfd41ed9
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 2%

---

# Icc配置檔案灰色{#iccprofilegray}

灰度預設輸出顏色配置檔案。 指定當未使用icc=指定輸出顏色空間時用於灰度響應影像的ICC顏色配置檔案的名稱，以及使用各種「影像服務」命令（如color=）指定的某些灰度顏色值的名稱。

## 屬性 {#section-03f090ee2acf4537b83f78840d23ecab}

文本字串。 如果指定，則必須是有效 `icc::Name` 此影像目錄或預設目錄或相對於 `attribute::RootPath`。 引用的ICC配置檔案必須是灰度配置檔案。

## 預設 {#section-95ba3ab15edc4259b657c6ebf8783d61}

繼承自 `default::IccProfileGray` 或為空。

## 另請參閱 {#section-b737b9a6a8bd4997b660292301ba967b}

[icc:：名稱](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) 。 [屬性：:IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f)。 [屬性：:IccProfileSrcGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9)。 [屬性：:RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
