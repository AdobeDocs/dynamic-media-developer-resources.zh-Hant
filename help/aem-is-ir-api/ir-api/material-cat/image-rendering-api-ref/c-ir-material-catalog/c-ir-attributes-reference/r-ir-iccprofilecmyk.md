---
description: CMYK預設顏色空間。 指定當未使用icc=指定輸出顏色空間時，用於灰度響應影像的ICC顏色配置檔案的名稱。
solution: Experience Manager
title: IccProfileCmyk
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: c36ea45d-dc91-4afa-825a-7af49738101c
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 3%

---

# IccProfileCmyk{#iccprofilecmyk}

CMYK預設顏色空間。 指定當未使用icc=指定輸出顏色空間時，用於灰度響應影像的ICC顏色配置檔案的名稱。

## 屬性 {#section-849678b272954bdcb236f49aa54f1609}

文字字串。 如果指定，則必須是此影像目錄或預設目錄的ICC配置檔案映射中的有效`icc::Name`值，或相對於`attribute::RootPath`的檔案路徑。 引用的ICC配置檔案必須是CMYK配置檔案。

## 預設 {#section-55026b7454af4d868bcb47f7743c9c5b}

如果未定義或為空，則從`default::IccProfileCmyk`繼承。

## 另請參閱 {#section-89feb193693b43dc99a2107658d57154}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) , [屬性：:IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40), [屬性：:IccProfileSrcCmyk](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilesrccmyk.md#reference-0256cae955404ebc92d5d0d1fa095ea2), [屬性：:RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
