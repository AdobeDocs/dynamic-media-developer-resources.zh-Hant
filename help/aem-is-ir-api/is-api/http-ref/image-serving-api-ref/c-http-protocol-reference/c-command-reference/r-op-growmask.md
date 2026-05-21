---
title: op_growMask
description: 膨脹/侵蝕影像。 套用形態學膨脹（半徑> 0）或侵蝕（半徑< 0）至遮色片資料。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 322d97af-bb1b-44bb-90f1-cda9984b78b5
TQID: 'https://experienceleague.adobe.com/-MDsQlyw5ts3RL59hw4-EeF146qdxZqc3fOfzL8BUOA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 103
ht-degree: 2%

---

# op_growMask{#op-growmask}

膨脹/侵蝕影像。 套用形態學膨脹（半徑> 0）或侵蝕（半徑&lt; 0）至遮色片資料。

`op_growMask= *`半徑`*`

<table id="simpletable_3BAA4523D29E447FA7A4C9009B3E8344"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname">半徑</span> </p> </td> 
  <td class="stentry"> <p>以畫素為單位擴大/侵蝕半徑，假設半徑適用於完整解析度遮色片，因此會針對縮減取樣遮色片(int -100..100)縮小半徑。 </p></td> 
 </tr> 
</table>

主要用於稍微增加或縮小遮色片，以避免遮色片邊緣出現不自然感。

## 屬性 {#section-b1c66d65168d4ea695e8662ea690bd4e}

套用至目前的圖層，或套用至圖層`0` （若為`layer=comp`）。

## 預設 {#section-14c908bb87cb42acbea709effea2f964}

`op_growMask=0`，無變更。

## 另請參閱 {#section-ad3e5cecfc3448a38ea06093e015c88a}

[圖層效果](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-layer-effects.md#reference-82a6b5311b3d4471ad2799adb3b2201c)

[op_grow](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-grow.md#reference-f95f3291c78c42b9a34b1b7e177e739a)

[op_growMaskR](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-growmaskr.md#reference-8092864159ae43c490821b9590d7709a)
