---
description: RTF字串中引用的所有字型都必須在預設目錄或當前影像目錄的字型映射檔案中可用，否則將返回錯誤。
solution: Experience Manager
title: 字型處理
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 1%

---


# 字型處理{#font-handling}

RTF字串中引用的所有字型都必須在預設目錄或當前影像目錄的字型映射檔案中可用，否則將返回錯誤。

對斜體和粗體文字進行註冊，可獲得最佳的品質。 如果不可用，伺服器可以從標準面合成粗體和／或斜體字型面。 (請參閱「` [attribute::SynthesizeFontStyles](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md#reference-1b12ba881b9146c793bcb07407cacb15)`」)。

在RTF字串中明確指定無時，使用`attribute::DefaultFont`指定的字型。

「影像伺服」支援TrueType、OpenType、Adobe Type1（僅限Windows）字型。

## Photofont®字型支援{#section-74560ae898cf4708aba4c8b4093f5f00}

`textPs=` 支援Photofont®字型，但有下列限制：

* `\cf` 在指定「Photofont」（像片字型）的文字範圍中忽略；Photofont字型面具有預先定義的顏色
* 不支援合成的字型樣式；使用`\b`和`\i`需要對應的字型對應項目，否則會傳回錯誤

* 不支援垂直文字流
* 不支援含16位元影像的Photofont字型
* 不支援每張影像具有多個字元的Photofont字型
* 除非Photofont字形影像內嵌色彩描述檔，否則套用天真的色彩轉換；在這種情況下，總是會套用相對比色演算方式和黑點補償

如需詳細資訊，請參閱` [www.photofont.com](http://www.photofont.com)`。

## 另請參閱 {#section-6cb8a802aa044836bbe449d559093f3a}

[字型對應參考](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-font-map-reference/c-font-map-reference.md#concept-f81f319d03c646c5a8ef87b3277dd37d)，屬 [性：:SynethingFontStyles](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md#reference-1b12ba881b9146c793bcb07407cacb15)，屬 [性：:DefaultFont](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultfont.md#reference-48b763ac254545e89a25c76ff7581107),  [ [!DNL www.photofont.com] ](http://www.photofont.com)
