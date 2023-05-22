---
description: 放大/腐蝕影像。 將形態膨脹（半徑> 0）或腐蝕（半徑< 0）應用於掩模資料。
solution: Experience Manager
title: op_grow掩碼
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 322d97af-bb1b-44bb-90f1-cda9984b78b5
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 2%

---

# op_grow掩碼{#op-growmask}

放大/腐蝕影像。 將形態膨脹（半徑> 0）或腐蝕（半徑&lt; 0）應用於掩模資料。

`op_growMask= *`半徑`*`

<table id="simpletable_3BAA4523D29E447FA7A4C9009B3E8344"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 半徑</span> </p> </td> 
  <td class="stentry"> <p>擴展/侵蝕半徑（以像素為單位），其中半徑假定應用於全解析度蒙版，因此縮放下採樣蒙版(int -100..100)。 </p></td> 
 </tr> 
</table>

主要用於略微生長或收縮蒙版，以避免蒙版邊緣周圍的偽像。

## 屬性 {#section-b1c66d65168d4ea695e8662ea690bd4e}

應用於當前圖層或圖層 `0` 如果 `layer=comp`。

## 預設 {#section-14c908bb87cb42acbea709effea2f964}

`op_growMask=0`，不更改。

## 另請參閱 {#section-ad3e5cecfc3448a38ea06093e015c88a}

[層效果](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-layer-effects.md#reference-82a6b5311b3d4471ad2799adb3b2201c)

[op_grow](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-grow.md#reference-f95f3291c78c42b9a34b1b7e177e739a)

[op_growMaskR](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-growmaskr.md#reference-8092864159ae43c490821b9590d7709a)
