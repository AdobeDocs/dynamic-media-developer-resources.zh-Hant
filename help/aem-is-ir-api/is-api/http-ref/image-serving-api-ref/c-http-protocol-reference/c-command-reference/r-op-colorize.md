---
description: 將影像上色。 在保留陰影和高光的同時對影像資料著色。
solution: Experience Manager
title: op_colorize
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1abbde32-867a-4596-a46b-12ec50d59170
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '313'
ht-degree: 4%

---

# op_colorize{#op-colorize}

將影像上色。 在保留陰影和高光的同時對影像資料著色。

` op_colorize= *``*[,off|norm[, *`colorcontrapt`*]]`

<table id="simpletable_768D6CDF3F734E7F89DC7AB2EAAC0C77"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> color </span> </p> </td> 
  <td class="stentry"> <p>替換RGB顏色。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 關閉 </span> </p> </td> 
  <td class="stentry"> <p>禁用自動亮度補償。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 規範  </span> </p> </td> 
  <td class="stentry"> <p>啟用自動亮度補償（預設）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 對比 </span> </p> </td> 
  <td class="stentry"> <p>對比度範圍（實數0.100）;設為0以保留輸入對比度。 </p> </td> 
 </tr> 
</table>

第二個參數指定在著色之前是否應調整源影像的亮度。 指定`off`以禁用自動亮度補償，或指定`norm`以自動調整亮度，使中值為50%的強度。

將&#x200B;*`contrast`*&#x200B;值設定為0以保留輸入影像的對比度範圍，或指定值大於0的所需對比度範圍。 值 100 會使對比最大化。一般值可能介於30和70之間。

除了內置亮度和對比度調整外，`op_brightness=`和`op_contrast=`還可用於進一步微調著色效果。

>[!NOTE]
>
>著色算法只使用影像資料中的亮度資訊。 這種灰度轉換簡單，不受色彩管理。 `op_colorize` 即使輸入為灰度或CMYK，仍始終輸出RGB資料。

## 屬性 {#section-c0f8bd424b864153a1108f384939f55b}

圖層命令。 若`layer=comp`，則套用至目前層或複合影像。 被效果層忽略。

*`color`* 必須是RGB值；不支援 *`color`* 灰色或CMYK值。

如果關閉亮度補償，則會忽略&#x200B;*`contrast`*&#x200B;值。

*`color`* 假定存在於對應於像素類型的工作顏色空 *`color`*&#x200B;間。*`color`* 如果在合併時圖層影像具有不同的像素類型，則精確地進行轉換。

在應用操作之前， CMYK影像將轉換為RGB。

## 預設 {#section-0c3ea13efbac432c8970862d223e39b3}

`None`，無色化。第二和第三個參數預設為`norm,0`，用於自動亮度補償和不更改對比度。

## 範例 {#section-4c418d7b5e97409d9a448b8f08a1eab3}

在對影像層著色之前動態調整亮度和對比度：

… `&op_brightness=-15&op_contrast=22&op_colorize=a0b0c0&`…

請改用自動亮度和對比度調整：

... `&op_colorize=a0b0c0,norm,50&`...

## 另請參閱 {#section-5581eb0e03014fa795e8f078c60e6c8d}

[color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md),  [op_brightness=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-brightness.md#reference-edf79dc41ae5411c80bec3ee3731c58a),  [op_contrast=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-contrast.md#reference-b26dfa9869fd43bebea0fbb8e9fe743d),  [Color Management](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
