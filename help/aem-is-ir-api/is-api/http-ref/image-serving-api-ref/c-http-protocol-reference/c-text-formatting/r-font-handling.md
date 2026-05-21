---
title: 字型處理
description: 在RTF字串中參照的所有字型都必須可在預設目錄或目前影像目錄的字型對應檔案中使用，否則會傳回錯誤。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f24edd53-4b21-4147-9b50-95e616279aa8
TQID: 'https://experienceleague.adobe.com/KMD5vdWHM8HYsCO6UtJpPpTBfg9VJufhvsFsfOJiHv8'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 134
ht-degree: 1%

---

# 字型處理{#font-handling}

在RTF字串中參照的所有字型都必須可在預設目錄或目前影像目錄的字型對應檔案中使用，否則會傳回錯誤。

登入對應的字型檔案即可獲得斜體及粗體文字的最佳品質。 如果不可用，伺服器可以從標準字型合成粗體和/或斜體字型。 (請參閱[屬性：：SynthesizeFontStyles](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md)。

在RTF字串中未明確指定字型時，會使用以`attribute::DefaultFont`指定的字型。

「影像伺服」支援TrueType、®、Adobe Type 1 （僅限Windows）字型。

<!--
 THIS APPEARS TO BE VERY OLD OUTDATED INFORMATION; URL IS DEAD TOO ## Photofont&reg; font support {#section-74560ae898cf4708aba4c8b4093f5f00}

Photofont&reg; fonts support `textPs=`, with the following restrictions:

* `\cf` is ignored in text spans that specify a Photofont font; Photofont font faces have predefined colors 
* Synthesized font styles are not supported; use of `\b` and `\i`require corresponding font map entries, otherwise an error is returned 

* Vertical text flow is not supported 
* Photofont fonts with 16-bit images are not supported 
* Photofont fonts with multiple glyphs per image are not supported 
* Naïve color conversion is applied unless the Photofont glyph images embed color profiles; in this case, relative colorimetric render intent and blackpoint compensation are always applied

See [https://www.photofont.com](https://www.photofont.com) for additional information.
-->

## 另請參閱 {#section-6cb8a802aa044836bbe449d559093f3a}

[字型對應參考](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-font-map-reference/c-font-map-reference.md#concept-f81f319d03c646c5a8ef87b3277dd37d)，[屬性：：SynthesizeFontStyles](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md#reference-1b12ba881b9146c793bcb07407cacb15)，[屬性：：DefaultFont](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultfont.md#reference-48b763ac254545e89a25c76ff7581107)
