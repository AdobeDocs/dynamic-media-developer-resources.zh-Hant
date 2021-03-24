---
description: 灰階預設輸入色彩描述檔。 指定不嵌入色彩描述檔的灰階材質影像所要使用的ICC色彩描述檔名稱。
solution: Experience Manager
title: IccProfileSrcGray
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 2%

---


# IccProfileSrcGray{#iccprofilesrcgray}

灰階預設輸入色彩描述檔。 指定不嵌入色彩描述檔的灰階材質影像所要使用的ICC色彩描述檔名稱。

## 屬性 {#section-97923d8561b845309442d57d017d91a4}

文字字串。 如果指定，則必須是此映像目錄或預設目錄的ICC配置檔案映射中的有效`icc::Name`值，或是相對於`attribute::RootPath`的檔案路徑。 參考的ICC配置檔案必須是灰度配置檔案。

## 預設 {#section-02c52805ee13483dba7878aeab51f889}

如果未定義或為空，則繼承自`default::IccProfileSrcGray`。 如果`attribute::IccProfileSrcGray`未解析為有效的配置式，則將改用`attribute::IccProfileGray`。

## 另請參閱 {#section-c361d6f6231942b3aa8b4b496e1d3de3}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) ,  [attribute::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40),  [attribute::IccProfileGray](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilegray.md#reference-712f1d0dcca748df9aaf495681bb39e6),  [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
