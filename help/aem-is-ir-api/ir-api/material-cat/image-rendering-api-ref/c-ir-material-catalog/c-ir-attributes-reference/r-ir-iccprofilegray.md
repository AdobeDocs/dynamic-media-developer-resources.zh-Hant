---
description: 灰階預設色域。 指定當未使用icc=指定輸出色域時，用於灰階響應影像的ICC顏色配置檔案的名稱。
solution: Experience Manager
title: IccProfileGray
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 3%

---


# IccProfileGray{#iccprofilegray}

灰階預設色域。 指定當未使用icc=指定輸出色域時，用於灰階響應影像的ICC顏色配置檔案的名稱。

## 屬性 {#section-7af0a3e2c8cf4cdd98974bfa4a15f3ac}

文字字串。 如果指定，則必須是此材料目錄或預設目錄的ICC配置檔案映射中的有效`icc::Name`值，或是相對於`attribute::RootPath`的檔案路徑。 參考的ICC配置檔案必須是灰度配置檔案。

## 預設 {#section-aaa1c71e5d0c4e0792099d77e37c05ee}

如果未定義或為空，則繼承自`default::IccProfileGray`。

## 另請參閱 {#section-cd43189611f4426aacddcc604eb02a10}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) ，屬 [性：:IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40)，屬 [性：:IccProfileSrcGray](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilesrcgray.md#reference-a2abcd4aa5864738bbea8f55706deaf2), [屬性：:RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
