---
description: 放大/腐蝕影像。 將形態膨脹（半徑> 0）或腐蝕（半徑< 0）應用於掩模資料。
solution: Experience Manager
title: op_growMaskR
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7abfbccf-8bcf-44d4-b50a-eca7a3f11360
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 3%

---

# op_growMaskR{#op-growmaskr}

放大/腐蝕影像。 將形態膨脹（半徑> 0）或腐蝕（半徑&lt; 0）應用於掩模資料。

`op_growMaskR= *`半徑R`*`

<table id="simpletable_3BAA4523D29E447FA7A4C9009B3E8344"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 半徑R</span></span> </p> </td> 
  <td class="stentry"> <p>擴展/侵蝕半徑（以像素為單位），其中 <span class="codeph"><span class="varname"> 半徑R</span></span> 按原樣應用，而不管蒙版是否下採樣(int -100..100)。 </p></td> 
 </tr> 
</table>

主要用於略微生長或收縮蒙版，以避免蒙版邊緣周圍的偽像。

## 屬性 {#section-b1c66d65168d4ea695e8662ea690bd4e}

應用於當前圖層或圖層 `0` 如果 `layer=comp`。

## 預設 {#section-14c908bb87cb42acbea709effea2f964}

`op_growMaskR=0`，不更改。

## 另請參閱 {#section-ad3e5cecfc3448a38ea06093e015c88a}

[層效果](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-layer-effects.md#reference-82a6b5311b3d4471ad2799adb3b2201c)

[op_grow](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-grow.md#reference-f95f3291c78c42b9a34b1b7e177e739a)

[op_grow掩碼](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-growmask.md#reference-f0f9000af3ae43aba73d3ac1826710a1)
