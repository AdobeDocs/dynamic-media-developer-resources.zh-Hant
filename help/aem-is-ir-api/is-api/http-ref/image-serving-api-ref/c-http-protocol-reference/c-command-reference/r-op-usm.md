---
title: op_usm
description: 不銳利化遮色片。 如果圖層=comp，則所有縮放之後，對圖層或最終檢視影像進行遮色片銳利化調整。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a83d6326-9029-4c5c-a069-92bc81120866
TQID: 'https://experienceleague.adobe.com/Q2-9E1SNDgr8rGYWNKDLlVcQU85EhpEXhxAqF3WrJic'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 151
ht-degree: 1%

---

# op_usm{#op-usm}

不銳利化遮色片。 如果圖層=comp，則所有縮放之後，對圖層或最終檢視影像進行遮色片銳利化調整。

假設引數會套用至完整解析度的影像，並在處理縮減取樣影像時按比例縮小。

`op_usm= *`數量`*[, *`半徑`*[, *`臨界值`*[, *`單色`*]]]`

<table id="simpletable_0697E3BCB45F41C494D93A6017ADD2BF"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname">金額</span></span> </p></td> 
  <td class="stentry"> <p>濾鏡強度係數（實數0...5）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname">半徑</span></span> </p></td> 
  <td class="stentry"> <p>濾鏡核心半徑，以畫素為單位（實數0...250）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname">閾值</span></span> </p></td> 
  <td class="stentry"> <p>濾鏡臨界值層級(int 0...255)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname">單色</span></span> </p></td> 
  <td class="stentry"> <p>設為0可分別套用至每個色彩元件，或設為1僅套用至影像亮度（強度）。 </p> <p> 已忽略灰階影像的<span class="codeph"><span class="varname">單色</span></span>。 </p></td> 
 </tr> 
</table>

圖層遮色片或複合遮色片也會銳利化。

## 屬性 {#section-fb5311b34d164946b74dadb32359518a}

圖層屬性或檢視屬性。 套用至目前圖層或最終檢視影像（若為`layer=comp`）。 被效果圖層忽略。

## 預設 {#section-2bedc99866ff473e90e5ea36596d8362}

`op_usm=0,0,0,0`不會產生遮色片銳利化調整效果。

## 另請參閱 {#section-63f186b8a1b34ec4bb895230838502a4}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) ， [op_sharpen=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-sharpen.md#reference-c32573230c6140f883efdaa201ea8541) ， [op_usmR](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-usmr.md#reference-c0168bc1e3a24370883670c09bcb0fef)
