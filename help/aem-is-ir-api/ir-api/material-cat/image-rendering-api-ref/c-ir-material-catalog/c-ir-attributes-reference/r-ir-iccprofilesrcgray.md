---
title: IccProfileSrcGray
description: 灰階預設輸入色彩設定檔。 指定用於未嵌入色彩設定檔之灰階材質影像的ICC色彩設定檔名稱。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8c89f0bb-4912-4838-a9e2-fb5d2f255eae
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 2%

---

# IccProfileSrcGray{#iccprofilesrcgray}

灰階預設輸入色彩設定檔。 指定用於未嵌入色彩設定檔之灰階材質影像的ICC色彩設定檔名稱。

## 屬性 {#section-97923d8561b845309442d57d017d91a4}

文字字串。 如果已指定，則必須是來自此影像目錄或預設目錄之ICC設定檔對映的有效`icc::Name`值，或是相對於`attribute::RootPath`的檔案路徑。 參照的ICC設定檔必須是灰階設定檔。

## 預設 {#section-02c52805ee13483dba7878aeab51f889}

如果未定義或空白，則繼承自`default::IccProfileSrcGray`。 如果`attribute::IccProfileSrcGray`未解析為有效的設定檔，則改用`attribute::IccProfileGray`。

## 另請參閱 {#section-c361d6f6231942b3aa8b4b496e1d3de3}

[icc：：Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) ，[attribute：：IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40)，[attribute：：IccProfileGray](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilegray.md#reference-712f1d0dcca748df9aaf495681bb39e6)，[attribute：：RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
