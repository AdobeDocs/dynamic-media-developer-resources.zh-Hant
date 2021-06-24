---
description: CMYK預設輸入顏色配置檔案。 指定用於未嵌入顏色配置檔案的CMYK材料影像的ICC顏色配置檔案的名稱。
solution: Experience Manager
title: IccProfileSrcCmyk
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 09be34c8-facc-40c3-ba15-c48bd93b3be1
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 3%

---

# IccProfileSrcCmyk{#iccprofilesrccmyk}

CMYK預設輸入顏色配置檔案。 指定用於未嵌入顏色配置檔案的CMYK材料影像的ICC顏色配置檔案的名稱。

## 屬性 {#section-0cee77438d914c319ec876edb3490821}

文字字串。 如果指定，則必須是此影像目錄或預設目錄的ICC配置檔案映射中的有效`icc::Name`值，或相對於`attribute::RootPath`的檔案路徑。 引用的ICC配置檔案必須是CMYK配置檔案。

## 預設 {#section-11f6239e0dd14827abf4a95c1b30161c}

如果未定義或為空，則從`default::IccProfileSrcCmyk`繼承。 如果`attribute::IccProfileSrcCmyk`未解析為有效的設定檔，則會改用`attribute::IccProfileCmyk`。

## 另請參閱 {#section-88adddd70265459a9a5d2f50829a4ba7}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) , [屬性：:IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40), [屬性：:IccProfileCmyk](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127), [屬性：:RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
