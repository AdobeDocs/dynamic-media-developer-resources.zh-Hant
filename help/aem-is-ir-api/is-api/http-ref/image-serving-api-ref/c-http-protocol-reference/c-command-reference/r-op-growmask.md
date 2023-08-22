---
title: op_growMask
description: 膨脹/侵蝕影像。 套用形態學膨脹（半徑> 0）或侵蝕（半徑< 0）至遮色片資料。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 322d97af-bb1b-44bb-90f1-cda9984b78b5
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 2%

---

# op_growMask{#op-growmask}

膨脹/侵蝕影像。 套用形態學膨脹（半徑> 0）或侵蝕（半徑&lt; 0）至遮色片資料。

`op_growMask= *`半徑`*`

<table id="simpletable_3BAA4523D29E447FA7A4C9009B3E8344"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 半徑</span> </p> </td> 
  <td class="stentry"> <p>以畫素為單位擴大/侵蝕半徑，假設半徑適用於完整解析度遮色片，因此會針對縮減取樣遮色片(int -100..100)縮小半徑。 </p></td> 
 </tr> 
</table>

主要用於稍微增加或縮小遮色片，以避免遮色片邊緣出現不自然感。

## 屬性 {#section-b1c66d65168d4ea695e8662ea690bd4e}

套用至目前的圖層或圖層 `0` 如果 `layer=comp`.

## 預設 {#section-14c908bb87cb42acbea709effea2f964}

`op_growMask=0`，不會變更。

## 另請參閱 {#section-ad3e5cecfc3448a38ea06093e015c88a}

[圖層效果](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-layer-effects.md#reference-82a6b5311b3d4471ad2799adb3b2201c)

[op_grow](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-grow.md#reference-f95f3291c78c42b9a34b1b7e177e739a)

[op_growMaskR](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-growmaskr.md#reference-8092864159ae43c490821b9590d7709a)
