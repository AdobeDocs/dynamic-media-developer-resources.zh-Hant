---
title: op_colorize
description: 將影像上色。 為影像資料上色，同時保留陰影和高光。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1abbde32-867a-4596-a46b-12ec50d59170
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '313'
ht-degree: 3%

---

# op_colorize{#op-colorize}

將影像上色。 為影像資料上色，同時保留陰影和高光。

` op_colorize= *`色彩`*[,off|norm[, *`對比`*]]`

<table id="simpletable_768D6CDF3F734E7F89DC7AB2EAAC0C77"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname">色彩</span> </p> </td> 
  <td class="stentry"> <p>取代RGB色彩。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph">折扣</span> </p> </td> 
  <td class="stentry"> <p>停用自動亮度補償。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph">標準</span> </p> </td> 
  <td class="stentry"> <p>啟用自動亮度補償（預設）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname">對比</span> </p> </td> 
  <td class="stentry"> <p>對比範圍（實數0..100）；設定為0可保留輸入對比。 </p> </td> 
 </tr> 
</table>

第二個引數會指定在彩色化之前是否應調整來源影像的亮度。 指定`off`以停用自動亮度補償，或指定`norm`以自動調整亮度，使中值達到50%強度。

將&#x200B;*`contrast`*&#x200B;值設定為0以保留輸入影像的對比範圍，或使用大於0的值指定所要的對比範圍。 值 100 會使對比最大化。一般值可能介於30到70之間。

除了內建的亮度和對比調整之外，`op_brightness=`和`op_contrast=`也可以用來進一步微調色彩效果。

>[!NOTE]
>
>彩色化演演算法只使用影像資料中的亮度資訊。 這種灰階轉換非常簡單，而且不受色彩管理。 `op_colorize`一律會輸出RGB資料，即使輸入是灰階或CMYK亦然。

## 屬性 {#section-c0f8bd424b864153a1108f384939f55b}

圖層指令。 套用至目前的圖層或複合影像（若為`layer=comp`）。 被效果圖層忽略。

*`color`*&#x200B;必須是RGB值；不支援灰色或CMYK *`color`*&#x200B;值。

如果關閉亮度補償，則會忽略&#x200B;*`contrast`*&#x200B;值。

假設&#x200B;*`color`*&#x200B;存在於與&#x200B;*`color`*&#x200B;的畫素型別對應的工作色域中。 如果圖層影像在合併時具有不同的畫素型別，則會精確轉換&#x200B;*`color`*。

CMYK影像會在套用作業之前轉換為RGB。

## 預設 {#section-0c3ea13efbac432c8970862d223e39b3}

`None`，無色彩化。 第二個和第三個引數預設為`norm,0`，用於自動亮度補償且對比度不會變更。

## 範例 {#section-4c418d7b5e97409d9a448b8f08a1eab3}

在色彩化影像圖層之前，動態調整亮度和對比：

... `&op_brightness=-15&op_contrast=22&op_colorize=a0b0c0&`...

請改用自動亮度及對比度調整：

... `&op_colorize=a0b0c0,norm,50&`...

## 另請參閱 {#section-5581eb0e03014fa795e8f078c60e6c8d}

[色彩](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)，[op_brightness=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-brightness.md#reference-edf79dc41ae5411c80bec3ee3731c58a)，[op_contrast=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-contrast.md#reference-b26dfa9869fd43bebea0fbb8e9fe743d)，[色彩管理](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
