---
title: op_grow
description: 膨脹/侵蝕影像。 將形態學膨脹（半徑> 0）或侵蝕（半徑< 0）套用至影像資料。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4c5bef4e-f80e-454d-8e93-30bf33d7ec9e
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 2%

---

# op_grow{#op-grow}

膨脹/侵蝕影像。 將形態學膨脹（半徑> 0）或侵蝕（半徑&lt; 0）套用至影像資料。

`op_grow= *`半徑`*`

<table id="simpletable_3BAA4523D29E447FA7A4C9009B3E8344"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname">半徑</span></span> </p> </td> 
  <td class="stentry"> <p>膨脹/侵蝕半徑，以畫素為單位(int -100..100)。 </p></td> 
 </tr> 
</table>

`*`半徑`*`是相對於複合影像的畫素。 如果影像為顏色，則會獨立處理每個元件。

主要用於修改圖層效果的大小。 在文字圖層或含遮色片的純色圖層上取得特殊效果也很有用。

## 屬性 {#section-b1c66d65168d4ea695e8662ea690bd4e}

圖層屬性。 套用至目前的圖層或複合影像（若為`layer=comp`）。

## 預設 {#section-14c908bb87cb42acbea709effea2f964}

`op_grow=0`，無變更。

## 另請參閱 {#section-ad3e5cecfc3448a38ea06093e015c88a}

[圖層效果](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-layer-effects.md#reference-82a6b5311b3d4471ad2799adb3b2201c)
