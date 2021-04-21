---
description: RGB預設輸入色彩描述檔。 指定ICC色彩描述檔的名稱，此描述檔用於未嵌入色彩描述檔的RGB材質影像和暈映，以及使用各種「影像演算」指令（例如bgc=和color=）指定的RGB色彩值。
solution: Experience Manager
title: IccProfileSrcRgb
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 2%

---


# IccProfileSrcRgb{#iccprofilesrcrgb}

RGB預設輸入色彩描述檔。 指定ICC色彩描述檔的名稱，此描述檔用於未嵌入色彩描述檔的RGB材質影像和暈映，以及使用各種「影像演算」指令（例如bgc=和color=）指定的RGB色彩值。

## 屬性 {#section-c22966bba03e43c08e9d3fb91bfdd465}

文字字串。 如果指定，則必須是此映像目錄或預設目錄的ICC配置檔案映射中的有效`icc::Name`值，或是相對於`attribute::RootPath`的檔案路徑。 參考的ICC描述檔必須是RGB描述檔。

## 預設 {#section-0171cd6680284bfa9844b9cc3644ca61}

如果未定義或為空，則繼承自`default::IccProfileSrcRgb`。 如果`attribute::IccProfileSrcRgb`未解析為有效的配置式，則改用`attribute::IccProfileRgb`。

## 另請參閱 {#section-1ba91666830f4c209c39260ea29f938e}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) ,  [attribute::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40),  [attribute::IccProfileRgb](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilergb.md#reference-cdaad25b155646ffa382d722fd324b30),  [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
