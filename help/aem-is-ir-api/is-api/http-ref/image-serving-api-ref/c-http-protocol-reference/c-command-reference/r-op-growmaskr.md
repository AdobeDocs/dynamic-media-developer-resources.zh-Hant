---
description: 膨脹／腐蝕影像。 對遮色片資料套用形態膨脹（半徑> 0）或腐蝕（半徑< 0）。
solution: Experience Manager
title: op_growMaskR
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 3%

---


# op_growMaskR{#op-growmaskr}

膨脹／腐蝕影像。 對遮色片資料套用形態膨脹（半徑> 0）或腐蝕（半徑&lt; 0）。

`op_growMaskR= *`radiusR`*`

<table id="simpletable_3BAA4523D29E447FA7A4C9009B3E8344"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> radiusR</span></span> </p> </td> 
  <td class="stentry"> <p>不論遮色片是否縮減取樣(int -100..100)，以像素為單位，其中<span class="codeph"><span class="varname">radiusR</span></span>按原樣套用。 </p></td> 
 </tr> 
</table>

主要用於微幅生長或收縮遮色片，以避免遮色片邊緣周圍出現偽影。

## 屬性 {#section-b1c66d65168d4ea695e8662ea690bd4e}

應用於當前層，如果`layer=comp`則應用於`0`層。

## 預設 {#section-14c908bb87cb42acbea709effea2f964}

`op_growMaskR=0`，而無變更。

## 另請參閱 {#section-ad3e5cecfc3448a38ea06093e015c88a}

[圖層效果](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-layer-effects.md#reference-82a6b5311b3d4471ad2799adb3b2201c)

[op_grow](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-grow.md#reference-f95f3291c78c42b9a34b1b7e177e739a)

[op_growMask](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-growmask.md#reference-f0f9000af3ae43aba73d3ac1826710a1)
