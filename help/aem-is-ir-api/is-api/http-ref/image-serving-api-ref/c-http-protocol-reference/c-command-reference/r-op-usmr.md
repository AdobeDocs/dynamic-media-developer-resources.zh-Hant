---
description: 不鋒利的面具。 如果layer=comp，則在進行所有縮放後，取消銳化會遮蔽圖層或最終視圖影像。
solution: Experience Manager
title: op_usmR
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 51a779be-568b-40e5-99d9-e875023a2b2c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 3%

---

# op_usmR{#op-usmr}

不鋒利的面具。 如果layer=comp，則在進行所有縮放後，取消銳化會遮蔽圖層或最終視圖影像。

不管是否發生下採樣，參數都按原樣應用。

`op_usmR= *`金額`*[, *`半徑R`*[, *`閾值`*[, *`單色`*]]]`

<table id="simpletable_0697E3BCB45F41C494D93A6017ADD2BF"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 量</span></span> </p></td> 
  <td class="stentry"> <p>過濾器強度因子（實數0..5）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 半徑R</span></span> </p></td> 
  <td class="stentry"> <p>篩選內核半徑（以像素為單位）（實數0...250）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 臨界值</span></span> </p></td> 
  <td class="stentry"> <p>篩選閾值級別(int 0...255)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 單色</span></span> </p></td> 
  <td class="stentry"> <p>設定為0以單獨應用於每個顏色分量，或設定為1以僅應用於影像亮度（強度）。 </p> <p><span class="codeph"> <span class="varname"> 單色</span></span> 忽略灰度影像。 </p> </td> 
 </tr> 
</table>

層掩模或複合掩模也被削尖。

## 屬性 {#section-fb5311b34d164946b74dadb32359518a}

層屬性或視圖屬性。 應用於當前圖層或最終視圖影像(如果 `layer=comp`。 效果層忽略它。

## 預設 {#section-2bedc99866ff473e90e5ea36596d8362}

`op_usmR=0,0,0,0` 不會產生明顯的掩蔽效應。

## 另請參閱 {#section-63f186b8a1b34ec4bb895230838502a4}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) 。 [op_shark=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-sharpen.md#reference-c32573230c6140f883efdaa201ea8541) 。 [op_usm](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-usm.md#reference-51ac75adadfe4346ab60953192d0a1aa)
