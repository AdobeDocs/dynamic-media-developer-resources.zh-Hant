---
title: op_usmR
description: 不銳利化遮色片。 如果圖層=comp，則所有縮放之後，對圖層或最終檢視影像進行遮色片銳利化調整。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 51a779be-568b-40e5-99d9-e875023a2b2c
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 2%

---

# op_usmR{#op-usmr}

不銳利化遮色片。 如果圖層=comp，則所有縮放之後，對圖層或最終檢視影像進行遮色片銳利化調整。

引數會依原樣套用，無論是否已發生縮減取樣。

`op_usmR= *`金額`*[, *`radiusR`*[, *`臨界值`*[, *`單色`*]]]`

<table id="simpletable_0697E3BCB45F41C494D93A6017ADD2BF"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname">金額</span></span> </p></td> 
  <td class="stentry"> <p>濾鏡強度係數（實數0...5）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> radiusR</span></span> </p></td> 
  <td class="stentry"> <p>濾鏡核心半徑，以畫素為單位（實數0...250）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname">閾值</span></span> </p></td> 
  <td class="stentry"> <p>濾鏡臨界值層級(int 0...255)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname">單色</span></span> </p></td> 
  <td class="stentry"> <p>設為0可分別套用至每個色彩元件，或設為1僅套用至影像亮度（強度）。 </p> <p>已忽略灰階影像的<span class="codeph"> <span class="varname">單色</span></span>。 </p> </td> 
 </tr> 
</table>

圖層遮色片或複合遮色片也會銳利化。

## 屬性 {#section-fb5311b34d164946b74dadb32359518a}

圖層屬性或檢視屬性。 套用至目前圖層或最終檢視影像（若為`layer=comp`）。 效果圖層會忽略它。

## 預設 {#section-2bedc99866ff473e90e5ea36596d8362}

`op_usmR=0,0,0,0`不會產生遮色片銳利化調整效果。

## 另請參閱 {#section-63f186b8a1b34ec4bb895230838502a4}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) ， [op_sharpen=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-sharpen.md#reference-c32573230c6140f883efdaa201ea8541) ， [op_usm](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-usm.md#reference-51ac75adadfe4346ab60953192d0a1aa)
