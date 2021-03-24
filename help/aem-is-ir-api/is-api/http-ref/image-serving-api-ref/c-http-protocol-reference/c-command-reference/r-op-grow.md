---
description: 膨脹／腐蝕影像。 對影像資料應用形態膨脹（半徑> 0）或腐蝕（半徑< 0）。
solution: Experience Manager
title: op_grow
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 3%

---


# op_grow{#op-grow}

膨脹／腐蝕影像。 對影像資料應用形態膨脹（半徑> 0）或腐蝕（半徑&lt; 0）。

`op_grow= *`半徑`*`

<table id="simpletable_3BAA4523D29E447FA7A4C9009B3E8344"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 半徑</span></span> </p> </td> 
  <td class="stentry"> <p>以像素為單位，縮放／腐蝕半徑(int -100..100)。 </p></td> 
 </tr> 
</table>

`*`相`*` 對於合成影像的半徑（像素）。如果影像是彩色，則會獨立處理每個元件。

主要用於修改圖層效果的大小。 此外，使用遮色片在文字圖層或純色圖層上產生特殊效果也很實用。

## 屬性 {#section-b1c66d65168d4ea695e8662ea690bd4e}

層屬性。 如果`layer=comp`，則套用至目前圖層或複合影像。

## 預設 {#section-14c908bb87cb42acbea709effea2f964}

`op_grow=0`，而無變更。

## 另請參閱 {#section-ad3e5cecfc3448a38ea06093e015c88a}

[圖層效果](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-layer-effects.md#reference-82a6b5311b3d4471ad2799adb3b2201c)
