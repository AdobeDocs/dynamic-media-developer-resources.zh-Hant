---
description: RGB預設輸出色彩描述檔。 指定當未使用icc=指定輸出色域時，用於RGB響應影像的ICC顏色配置檔案的名稱，以及使用各種「影像渲染」命令（如bgc=和color=）指定的特定RGB顏色值。
solution: Experience Manager
title: IccProfileRgb
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 2%

---


# IccProfileRgb{#iccprofilergb}

RGB預設輸出色彩描述檔。 指定當未使用icc=指定輸出色域時，用於RGB響應影像的ICC顏色配置檔案的名稱，以及使用各種「影像渲染」命令（如bgc=和color=）指定的特定RGB顏色值。

## 屬性 {#section-b4a1bd92e99047479a5036413525a6d9}

文字字串。 如果指定，則必須是此材料目錄或預設目錄的ICC配置檔案映射中的有效`icc::Name`值，或是相對於`attribute::RootPath`的檔案路徑。 參考的ICC描述檔必須是RGB描述檔。

## 預設 {#section-5809772f8e96438ab7626d323c66a4ba}

如果未定義或為空，則繼承自`default::IccProfileRgb`。

## 另請參閱 {#section-732c17dece3a4575855c9b79a08d0067}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) ，屬 [性：:IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40)，屬 [性：:IccProfileSrcRgb](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilesrcrgb.md#reference-2fb0f7cfc6e74813b82cd98ae165bd49), [屬性：:RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
