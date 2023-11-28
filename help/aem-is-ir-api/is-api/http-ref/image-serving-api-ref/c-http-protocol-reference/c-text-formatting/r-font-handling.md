---
title: 字型處理
description: 在RTF字串中參照的所有字型都必須可在預設目錄或目前影像目錄的字型對應檔案中使用，否則會傳回錯誤。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f24edd53-4b21-4147-9b50-95e616279aa8
source-git-commit: e8e3ce9850ab8059aed81e720574d0c93f867a22
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 字型處理{#font-handling}

在RTF字串中參照的所有字型都必須可在預設目錄或目前影像目錄的字型對應檔案中使用，否則會傳回錯誤。

登入對應的字型檔案即可獲得斜體及粗體文字的最佳品質。 如果不可用，伺服器可以從標準字型合成粗體和/或斜體字型。 (請參閱 [attribute：：SynthesizeFontStyles](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md).

指定的字型 `attribute::DefaultFont` 當RTF字串中未明確指定任何專案時使用。

「影像伺服」支援TrueType、OpenType®、Adobe Type1 （僅限Windows）字型。

<!-- THIS APPEARS TO BE VERY OLD OUTDATED INFORMATION; URL IS DEAD TOO ## Photofont&reg; font support {#section-74560ae898cf4708aba4c8b4093f5f00}

Photofont&reg; fonts support `textPs=`, with the following restrictions:

* `\cf` is ignored in text spans that specify a Photofont font; Photofont font faces have predefined colors 
* Synthesized font styles are not supported; use of `\b` and `\i`require corresponding font map entries, otherwise an error is returned 

* Vertical text flow is not supported 
* Photofont fonts with 16-bit images are not supported 
* Photofont fonts with multiple glyphs per image are not supported 
* Naïve color conversion is applied unless the Photofont glyph images embed color profiles; in this case, relative colorimetric render intent and blackpoint compensation are always applied

See [https://www.photofont.com](https://www.photofont.com) for additional information. -->

## 另請參閱 {#section-6cb8a802aa044836bbe449d559093f3a}

[字型地圖參考](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-font-map-reference/c-font-map-reference.md#concept-f81f319d03c646c5a8ef87b3277dd37d)， [attribute：：SynthesizeFontStyles](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md#reference-1b12ba881b9146c793bcb07407cacb15)， [attribute：：DefaultFont](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultfont.md#reference-48b763ac254545e89a25c76ff7581107)
