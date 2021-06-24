---
description: 基於解析度的影像縮放。 將影像縮放至要求的解析度。
solution: Experience Manager
title: res
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: e8ed7b00-7bb3-463e-9aaa-47f77bd4b45e
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '328'
ht-degree: 1%

---

# res{#res}

基於解析度的影像縮放。 將影像縮放至要求的解析度。

` res= *`val`*`

<table id="simpletable_E69F3709266749C4A165C90FF18FF5AA"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val  </span> </p> </td> 
  <td class="stentry"> <p>目標解析度；通常以像素/英吋（實數）表示。 </p> </td> 
 </tr> 
</table>

比例因子是按&#x200B;*`val`*&#x200B;除以`catalog::Resolution`計算的。 請注意，此命令不影響回復影像的打印解析度。

要使用此功能，必須知道原始源影像的解析度並在`catalog::Resolution`中設定。 根據應用，解析度單元可能不同。 對於可重複的2D紋理或材料色板，如壁紙或織物，解析度可以表示為像素/英吋或像素/毫米。 航拍照片和地圖的提供方式可以按像素/英里或像素/公里進行。 在任何情況下，用於`catalog::Resolution`的單位必須與用於`res=`的單位相同。

除了以精確解析度獲得影像外，`res=`還可以用於以相同解析度合併多個影像，使這些影像中可見的項目彼此成準確比例。

>[!NOTE]
>
>通常，複合影像在返回到客戶端之前，會調整為目標視圖大小（由`wid=`、`hei=`或`attribute::DefaultPix`指定）。 為防止此調整大小並獲得具有`res=`所指定的精確解析度的影像，可能需要通過顯式指定`scl=1`禁用視圖縮放。 這會指示伺服器將複合影像裁切為目標檢視大小，而非縮放。

## 屬性 {#section-fdbd16e59cff4952a3717146bc91412e}

源影像/掩碼屬性。 被未與源影像或掩碼關聯的層忽略。 已為`layer=comp`指定應用到層0。 若為相同層指定`scale=`或`size=`，則忽略。

## 預設 {#section-c5f1ba6fe53d46eca32e7d0588dcdf3d}

如果未指定，`scale=`或`size=`將確定縮放因子，或者，如果未指定，則不使用縮放來使用影像。

## 範例 {#section-eb06f333e08e4247971fb1b18922597b}

以12像素/英吋的對象解析度檢索紋理影像，以用於影像渲染或影像創作。 我們指定了無損耗的PNG格式和更好的質量重採樣，以獲得盡可能高的質量。

` http:// *`伺服器`*/myTexture?res=12&fmt=png&resMode=sharp`

## 另請參閱 {#section-1f8a8f11772e493ca803c4511f397a11}

[catalog:：解析度](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1) ,  [attribute::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1),  [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc),  [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
