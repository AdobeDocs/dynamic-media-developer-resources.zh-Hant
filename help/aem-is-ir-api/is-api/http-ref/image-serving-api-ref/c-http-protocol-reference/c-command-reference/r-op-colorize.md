---
description: 為影像上色。 為影像資料上色，同時保留陰影和亮部。
seo-description: 為影像上色。 為影像資料上色，同時保留陰影和亮部。
seo-title: op_colorize
solution: Experience Manager
title: op_colorize
topic: Scene7 Image Serving - Image Rendering API
uuid: e74a85ca-73bf-4c69-ac77-768a58b33d0b
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150

---


# op_colorize{#op-colorize}

為影像上色。 為影像資料上色，同時保留陰影和亮部。

` op_colorize= *`色`*[,off|norm[, *`彩對比`*]]`

<table id="simpletable_768D6CDF3F734E7F89DC7AB2EAAC0C77"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> color </span> </p> </td> 
  <td class="stentry"> <p>取代RGB色彩。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 關閉 </span> </p> </td> 
  <td class="stentry"> <p>禁用自動亮度補償。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 規範 </span> </p> </td> 
  <td class="stentry"> <p>啟用自動亮度補償（預設）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 對比 </span> </p> </td> 
  <td class="stentry"> <p>對比範圍（實數0.100）;設為0可保留輸入對比度。 </p> </td> 
 </tr> 
</table>

第二個參數指定在上色前是否應調整源影像的亮度。 指定 `off` 停用自動亮度補償或 `norm` 自動調整亮度，使中值的強度為50%。

Set the *`contrast`* value to 0 to preserve the contrast range of the input image, or specify a desired contrast range with a value greater than 0. 值 100 會使對比最大化。典型值可能介於30到70之間。

除了內置亮度和對比度調整外， `op_brightness=``op_contrast=` 還可用於進一步微調著色效果。

>[!NOTE]
>
>上色算法只使用影像資料中的亮度資訊。 這種灰階轉換簡單，不受色彩管理。 `op_colorize` 即使輸入為灰階或CMYK，也一律會輸出RGB資料。

## 屬性 {#section-c0f8bd424b864153a1108f384939f55b}

圖層命令。 應用於當前圖層或複合影像（如果） `layer=comp`。 被效果圖層忽略。

*`color`* 必須是RGB值；不支援 *`color`* 灰色或CMYK值。

如果 *`contrast`* 關閉亮度補償，則忽略該值。

*`color`* 假定存在於與像素類型對應的工作顏色空間中 *`color`*。 *`color`* 如果圖層影像在合併時具有不同的像素類型，則可精確地轉換。

在應用操作之前，CMYK影像將轉換為RGB。

## 預設 {#section-0c3ea13efbac432c8970862d223e39b3}

`None`，無色化。 第二個和第三個引數預設為 `norm,0`自動亮度補償且不改變對比度。

## 範例 {#section-4c418d7b5e97409d9a448b8f08a1eab3}

在對影像圖層上色之前，動態調整亮度和對比：

… `&op_brightness=-15&op_contrast=22&op_colorize=a0b0c0&`…

請改用自動亮度和對比調整：

… `&op_colorize=a0b0c0,norm,50&`…

## 另請參閱 {#section-5581eb0e03014fa795e8f078c60e6c8d}

[color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md), [op_brightness=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-brightness.md#reference-edf79dc41ae5411c80bec3ee3731c58a), [op_contrast=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-contrast.md#reference-b26dfa9869fd43bebea0fbb8e9fe743d)，色彩管 [理](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
