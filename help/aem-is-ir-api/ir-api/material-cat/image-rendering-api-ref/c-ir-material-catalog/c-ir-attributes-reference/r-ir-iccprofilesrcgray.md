---
description: 灰階預設輸入色彩描述檔。 指定不嵌入色彩描述檔的灰階材質影像所要使用的ICC色彩描述檔名稱。
seo-description: 灰階預設輸入色彩描述檔。 指定不嵌入色彩描述檔的灰階材質影像所要使用的ICC色彩描述檔名稱。
seo-title: IccProfileSrcGray
solution: Experience Manager
title: IccProfileSrcGray
topic: Scene7 Image Serving - Image Rendering API
uuid: e05d1185-ffd6-4c04-a2b8-52228beae37d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# IccProfileSrcGray{#iccprofilesrcgray}

灰階預設輸入色彩描述檔。 指定不嵌入色彩描述檔的灰階材質影像所要使用的ICC色彩描述檔名稱。

## 屬性 {#section-97923d8561b845309442d57d017d91a4}

文字字串。 如果指定，則必須是此映 `icc::Name` 像目錄或預設目錄的ICC配置檔案映射中的有效值，或相對於的檔案路徑 `attribute::RootPath`。 參考的ICC配置檔案必須是灰度配置檔案。

## 預設 {#section-02c52805ee13483dba7878aeab51f889}

繼承自 `default::IccProfileSrcGray` （如果未定義或為空）。 如果 `attribute::IccProfileSrcGray` 未解析為有效的描述檔，則 `attribute::IccProfileGray` 會改用它。

## 另請參閱 {#section-c361d6f6231942b3aa8b4b496e1d3de3}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) , [attribute::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40), [attribute::IccProfileGray](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilegray.md#reference-712f1d0dcca748df9aaf495681bb39e6), [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
