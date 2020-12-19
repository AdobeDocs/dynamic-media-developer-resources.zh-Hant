---
description: 遮色片銳利化。 如果layer=comp，在進行所有縮放後，不銳利化會遮色圖層或最終檢視影像。
seo-description: 遮色片銳利化。 如果layer=comp，在進行所有縮放後，不銳利化會遮色圖層或最終檢視影像。
seo-title: op_usmR
solution: Experience Manager
title: op_usmR
topic: Scene7 Image Serving - Image Rendering API
uuid: 98afd83c-097e-40b4-b0a6-647f70b95fae
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 3%

---


# op_usmR{#op-usmr}

遮色片銳利化。 如果layer=comp，在進行所有縮放後，不銳利化會遮色圖層或最終檢視影像。

參數會依原樣套用，不論是否發生下採樣。

`op_usmR= *`AmountradiusRthremold單色`*[, *``*[, *``*[, *``*]]]`

<table id="simpletable_0697E3BCB45F41C494D93A6017ADD2BF"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 量</span></span> </p></td> 
  <td class="stentry"> <p>濾鏡強度系數（實數0...5）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> radiusR</span></span> </p></td> 
  <td class="stentry"> <p>以像素為單位的濾鏡核心半徑（實數0...250）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 臨界值</span></span> </p></td> 
  <td class="stentry"> <p>篩選臨界值層級(int 0...255)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 單色</span></span> </p></td> 
  <td class="stentry"> <p>設為0可分別套用至每個顏色元件，或設為1可僅套用至影像亮度（強度）。 </p> <p><span class="codeph"> <span class="varname"> 灰</span></span> 度影像忽略單色。 </p> </td> 
 </tr> 
</table>

圖層遮色片或複合遮色片也會銳利化。

## 屬性 {#section-fb5311b34d164946b74dadb32359518a}

層屬性或視圖屬性。 如果`layer=comp`，則套用至目前圖層或最終檢視影像。 效果圖層會忽略它。

## 預設 {#section-2bedc99866ff473e90e5ea36596d8362}

`op_usmR=0,0,0,0` 不會產生銳利的遮色片效果。

## 另請參閱 {#section-63f186b8a1b34ec4bb895230838502a4}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) ,  [op_sharpen=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-sharpen.md#reference-c32573230c6140f883efdaa201ea8541) ,  [op_usm](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-usm.md#reference-51ac75adadfe4346ab60953192d0a1aa)
