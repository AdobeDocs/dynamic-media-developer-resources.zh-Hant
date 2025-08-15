---
title: IccProfileRgb
description: RGB預設輸出色彩設定檔。 指定icc=未指定輸出色域時，用於RGB回應影像的ICC色彩設定檔名稱。 此外，對於使用各種「影像演算」指令（例如bgc=和color=）指定的某些RGB色彩值，也是如此。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4057e968-24de-41af-9901-a6cb5ed9ea63
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 2%

---

# IccProfileRgb{#iccprofilergb}

RGB預設輸出色彩設定檔。 指定當沒有使用`icc=`指定輸出色域時，用於RGB回應影像的ICC色彩設定檔名稱。 此外，對於使用各種影像演算命令指定的某些RGB色彩值，例如`bgc=`和`color=`。

## 屬性 {#section-b4a1bd92e99047479a5036413525a6d9}

文字字串。 如果已指定，則必須是來自此材質目錄或預設目錄之ICC設定檔對映的有效`icc::Name`值，或是相對於`attribute::RootPath`的檔案路徑。 參考的ICC設定檔必須是RGB設定檔。

## 預設 {#section-5809772f8e96438ab7626d323c66a4ba}

如果未定義或空白，則繼承自`default::IccProfileRgb`。

## 另請參閱 {#section-732c17dece3a4575855c9b79a08d0067}

[icc：：Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) ， [attribute：：IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40)， [attribute：：IccProfileSrcRgb](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilesrcrgb.md#reference-2fb0f7cfc6e74813b82cd98ae165bd49)， [attribute：：RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
