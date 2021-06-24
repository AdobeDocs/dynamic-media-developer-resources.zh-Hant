---
description: 膨脹/腐蝕影像。 對影像資料套用形態膨脹（半徑> 0）或腐蝕（半徑< 0）。
solution: Experience Manager
title: op_grow
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 4c5bef4e-f80e-454d-8e93-30bf33d7ec9e
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 3%

---

# op_grow{#op-grow}

膨脹/腐蝕影像。 對影像資料套用形態膨脹（半徑> 0）或腐蝕（半徑&lt; 0）。

`op_grow= *`半徑`*`

<table id="simpletable_3BAA4523D29E447FA7A4C9009B3E8344"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 半徑</span></span> </p> </td> 
  <td class="stentry"> <p>以像素為單位，延展/腐蝕半徑(int -100..100)。 </p></td> 
 </tr> 
</table>

`*``*` 弧度（相對於複合影像）以像素為單位。如果影像為顏色，則每個元件會獨立處理。

主要用於修改圖層效果的大小。 對於文本層或帶遮色片的實色層來說，也非常有用。

## 屬性 {#section-b1c66d65168d4ea695e8662ea690bd4e}

層屬性。 若`layer=comp`，則套用至目前層或複合影像。

## 預設 {#section-14c908bb87cb42acbea709effea2f964}

`op_grow=0`，無變更。

## 另請參閱 {#section-ad3e5cecfc3448a38ea06093e015c88a}

[圖層效果](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-layer-effects.md#reference-82a6b5311b3d4471ad2799adb3b2201c)
