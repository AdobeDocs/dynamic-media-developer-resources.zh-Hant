---
description: 不銳利化。 如果layer=comp，則在所有縮放後，不銳利化會遮色圖層或最終視圖影像。
solution: Experience Manager
title: op_usm
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a83d6326-9029-4c5c-a069-92bc81120866
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 6%

---

# op_usm{#op-usm}

不銳利化。 如果layer=comp，則在所有縮放後，不銳利化會遮色圖層或最終視圖影像。

假定這些參數應用於全解析度影像，並在處理縮減採樣的影像時縮放。

`op_usm= *``*[, *``*[, *``*[, *`amount tradusthreshold單色`*]]]`

<table id="simpletable_0697E3BCB45F41C494D93A6017ADD2BF"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 量</span></span> </p></td> 
  <td class="stentry"> <p>過濾器強度因子（實數0...5）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 半徑</span></span> </p></td> 
  <td class="stentry"> <p>以像素為單位篩選內核半徑（實數0...250）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 臨界值</span></span> </p></td> 
  <td class="stentry"> <p>篩選閾值級別(int 0...255)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 單色</span></span> </p></td> 
  <td class="stentry"> <p>設定為0以分別應用於每個顏色分量，或設定為1以僅應用於影像亮度（強度）。 </p> <p> <span class="codeph"><span class="varname"> </span></span> 灰階影像會忽略單色。 </p></td> 
 </tr> 
</table>

圖層蒙版或複合蒙版也被銳化。

## 屬性 {#section-fb5311b34d164946b74dadb32359518a}

層屬性或視圖屬性。 若`layer=comp`，則套用至目前層或最終檢視影像。 被效果層忽略。

## 預設 {#section-2bedc99866ff473e90e5ea36596d8362}

`op_usm=0,0,0,0` 不會產生銳利的遮蔽效果。

## 另請參閱 {#section-63f186b8a1b34ec4bb895230838502a4}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) ,  [op_sharpen=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-sharpen.md#reference-c32573230c6140f883efdaa201ea8541) ,  [op_usmR](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-usmr.md#reference-c0168bc1e3a24370883670c09bcb0fef)
