---
description: 膨脹/腐蝕影像。 將形態膨脹（半徑> 0）或腐蝕（半徑< 0）套用至遮色片資料。
solution: Experience Manager
title: op_growMaskR
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 7abfbccf-8bcf-44d4-b50a-eca7a3f11360
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 4%

---

# op_growMaskR{#op-growmaskr}

膨脹/腐蝕影像。 將形態膨脹（半徑> 0）或腐蝕（半徑&lt; 0）套用至遮色片資料。

`op_growMaskR= *`radiusR`*`

<table id="simpletable_3BAA4523D29E447FA7A4C9009B3E8344"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> radiusR</span></span> </p> </td> 
  <td class="stentry"> <p>以像素表示，其中<span class="codeph"><span class="varname"> radiusR</span></span>按原樣應用，而無論蒙版是否縮減取樣(int -100..100)。 </p></td> 
 </tr> 
</table>

主要用於稍微生長或縮小遮罩以避免遮罩邊緣周圍出現偽影。

## 屬性 {#section-b1c66d65168d4ea695e8662ea690bd4e}

應用於當前層，如果`layer=comp`則應用於`0`層。

## 預設 {#section-14c908bb87cb42acbea709effea2f964}

`op_growMaskR=0`，無變更。

## 另請參閱 {#section-ad3e5cecfc3448a38ea06093e015c88a}

[圖層效果](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-layer-effects.md#reference-82a6b5311b3d4471ad2799adb3b2201c)

[op_grow](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-grow.md#reference-f95f3291c78c42b9a34b1b7e177e739a)

[op_growMask](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-growmask.md#reference-f0f9000af3ae43aba73d3ac1826710a1)
