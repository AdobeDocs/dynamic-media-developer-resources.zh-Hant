---
description: 膨脹／腐蝕影像。 對遮色片資料套用形態膨脹（半徑> 0）或腐蝕（半徑< 0）。
seo-description: 膨脹／腐蝕影像。 對遮色片資料套用形態膨脹（半徑> 0）或腐蝕（半徑< 0）。
seo-title: op_growMask
solution: Experience Manager
title: op_growMask
topic: Scene7 Image Serving - Image Rendering API
uuid: 016501e8-33c5-4c9e-8d26-120b1e929c55
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# op_growMask{#op-growmask}

膨脹／腐蝕影像。 對遮色片資料套用形態膨脹（半徑> 0）或腐蝕（半徑&lt; 0）。

`op_growMask= *`半徑`*`

<table id="simpletable_3BAA4523D29E447FA7A4C9009B3E8344"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 半徑</span> </p> </td> 
  <td class="stentry"> <p>放大／腐蝕半徑（以像素為單位），其中半徑假設套用至完整解析度遮色片，因此會針對縮減取樣遮色片縮小(int -100..100)。 </p></td> 
 </tr> 
</table>

主要用於微幅生長或收縮遮色片，以避免遮色片邊緣周圍出現偽影。

## 屬性 {#section-b1c66d65168d4ea695e8662ea690bd4e}

應用於當前層，或應用於 `0` 層(如 `layer=comp`果)。

## 預設 {#section-14c908bb87cb42acbea709effea2f964}

`op_growMask=0`，而無變更。

## 另請參閱 {#section-ad3e5cecfc3448a38ea06093e015c88a}

[圖層效果](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-layer-effects.md#reference-82a6b5311b3d4471ad2799adb3b2201c)

[op_grow](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-grow.md#reference-f95f3291c78c42b9a34b1b7e177e739a)

[op_growMaskR](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-growmaskr.md#reference-8092864159ae43c490821b9590d7709a)
