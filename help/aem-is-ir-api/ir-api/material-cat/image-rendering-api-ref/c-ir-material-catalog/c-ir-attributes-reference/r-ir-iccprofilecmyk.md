---
description: CMYK預設色域。 指定當未使用icc=指定輸出色域時，用於灰階回應影像的ICC色彩描述檔名稱。
solution: Experience Manager
title: IccProfileCmyk
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 3%

---


# IccProfileCmyk{#iccprofilecmyk}

CMYK預設色域。 指定當未使用icc=指定輸出色域時，用於灰階回應影像的ICC色彩描述檔名稱。

## 屬性 {#section-849678b272954bdcb236f49aa54f1609}

文字字串。 如果指定，則必須是此映像目錄或預設目錄的ICC配置檔案映射中的有效`icc::Name`值，或是相對於`attribute::RootPath`的檔案路徑。 參考的ICC描述檔必須是CMYK描述檔。

## 預設 {#section-55026b7454af4d868bcb47f7743c9c5b}

如果未定義或為空，則繼承自`default::IccProfileCmyk`。

## 另請參閱 {#section-89feb193693b43dc99a2107658d57154}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) ，屬 [性：:IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40)，屬 [性：:IccProfileSrcCmyk](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilesrccmyk.md#reference-0256cae955404ebc92d5d0d1fa095ea2), [屬性：:RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
