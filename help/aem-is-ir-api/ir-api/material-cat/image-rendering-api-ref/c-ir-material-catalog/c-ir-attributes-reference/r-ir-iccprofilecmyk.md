---
description: CMYK預設色域。 指定當未使用icc=指定輸出色域時，用於灰階回應影像的ICC色彩描述檔名稱。
seo-description: CMYK預設色域。 指定當未使用icc=指定輸出色域時，用於灰階回應影像的ICC色彩描述檔名稱。
seo-title: IccProfileCmyk
solution: Experience Manager
title: IccProfileCmyk
topic: Scene7 Image Serving - Image Rendering API
uuid: d923d0fd-f00b-4fce-8ce9-8b177b4dba96
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# IccProfileCmyk{#iccprofilecmyk}

CMYK預設色域。 指定當未使用icc=指定輸出色域時，用於灰階回應影像的ICC色彩描述檔名稱。

## 屬性 {#section-849678b272954bdcb236f49aa54f1609}

文字字串。 如果指定，則必須是此映 `icc::Name` 像目錄或預設目錄的ICC配置檔案映射中的有效值，或相對於的檔案路徑 `attribute::RootPath`。 參考的ICC描述檔必須是CMYK描述檔。

## 預設 {#section-55026b7454af4d868bcb47f7743c9c5b}

繼承自 `default::IccProfileCmyk` （如果未定義或為空）。

## 另請參閱 {#section-89feb193693b43dc99a2107658d57154}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) ，屬 [性：:IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40)，屬 [性：:IccProfileSrcCmyk](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilesrccmyk.md#reference-0256cae955404ebc92d5d0d1fa095ea2), [屬性：:RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
