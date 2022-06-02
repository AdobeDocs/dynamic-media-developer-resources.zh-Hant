---
title: 字型處理
description: RTF字串中引用的所有字型必須在預設目錄或當前影像目錄的字型映射檔案中可用，否則將返回錯誤。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f24edd53-4b21-4147-9b50-95e616279aa8
source-git-commit: e1f0f8bdac2b7a8397adac3bb9ba38d0c519f8fb
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 0%

---

# 字型處理{#font-handling}

RTF字串中引用的所有字型必須在預設目錄或當前影像目錄的字型映射檔案中可用，否則將返回錯誤。

斜體和粗體文本的最佳質量是通過註冊相應的字型檔案來實現的。 如果不可用，伺服器可從標準面合成粗體和/或斜體字面。 (請參閱 [屬性：:SynethatedFontStyles](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md)。

指定的字型 `attribute::DefaultFont` 在RTF字串中顯式指定任何項時使用。

Image Serving支援TrueType、OpenType、Adobe Type1（僅限Windows）字型。

## Photofont®字型支援 {#section-74560ae898cf4708aba4c8b4093f5f00}

`textPs=` 支援Photofont®字型，但有以下限制：

* `\cf` 在指定Photofont字型的文本範圍中忽略；照片字型面具有預定義顏色
* 不支援合成字型樣式；使用 `\b` 和 `\i`需要相應的字型映射條目，否則返回錯誤

* 不支援垂直文本流
* 不支援帶有16位影像的Photofont字型
* 不支援每個影像具有多個字形的照片字型
* 除非Photofont字形影像嵌入了顏色配置檔案，否則將應用天真的顏色轉換；在這種情況下，始終應用相對比色渲染意圖和黑點補償

請參閱 [www.photofont.com](https://www.photofont.com) 的雙曲餘切值。

## 另請參閱 {#section-6cb8a802aa044836bbe449d559093f3a}

[字型映射引用](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-font-map-reference/c-font-map-reference.md#concept-f81f319d03c646c5a8ef87b3277dd37d)。 [屬性：:SynethatedFontStyles](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md#reference-1b12ba881b9146c793bcb07407cacb15)。 [屬性：:DefaultFont](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultfont.md#reference-48b763ac254545e89a25c76ff7581107)。 [ [!DNL www.photofont.com] ](https://www.photofont.com)
