---
title: IccProfileRgb
description: RGB預設輸出顏色配置檔案。 指定在未使用icc=指定輸出顏色空間時用於RGB響應影像的ICC顏色配置檔案的名稱。 也適用於使用各種「影像渲染」命令（如bgc=和color=）指定的某些RGB顏色值。
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

RGB預設輸出顏色配置檔案。 指定在未指定輸出顏色空間時用於RGB響應影像的ICC顏色配置檔案的名稱 `icc=`。 也適用於使用各種「影像渲染」命令指定的某些RGB顏色值，如 `bgc=` 和 `color=`。

## 屬性 {#section-b4a1bd92e99047479a5036413525a6d9}

文本字串。 如果指定，則必須是有效 `icc::Name` 此材料目錄或預設目錄的ICC配置檔案映射中的值，或相對於 `attribute::RootPath`。 引用的ICC配置檔案必須是RGB配置檔案。

## 預設 {#section-5809772f8e96438ab7626d323c66a4ba}

繼承自 `default::IccProfileRgb` 或為空。

## 另請參閱 {#section-732c17dece3a4575855c9b79a08d0067}

[icc:：名稱](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) 。 [屬性：:IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40)。 [屬性：:IccProfileSrcRgb](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilesrcrgb.md#reference-2fb0f7cfc6e74813b82cd98ae165bd49)。 [屬性：:RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
