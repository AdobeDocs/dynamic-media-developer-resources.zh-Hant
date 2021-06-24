---
description: 物質解析度。 指定可重複紋理或傾斜影像的解析度。
solution: Experience Manager
title: res
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: f207355d-5819-47fc-bda5-27a411449569
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 3%

---

# res{#res}

物質解析度。 指定可重複紋理或傾斜影像的解析度。

` res= *`val`*`

<table id="simpletable_2004B804D46E43C090E59BBFF8144598"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val  </span> </p> </td> 
  <td class="stentry"> <p>決議；材料解析度單位（通常為每英吋像素）（實數）。 </p> </td> 
 </tr> 
</table>

若是傾倒材料，如果同時指定`size=`和`res=`，則使用`size=`。

## 屬性 {#section-6a458ddc202f46e0b668c9f040a65cef}

材料屬性。 被實色材料忽略。 只有在同時使用紋理時，才通過機箱和窗口覆蓋材料。

## 預設 {#section-ee4088a994014df59105fc1dbb2aa042}

`catalog::Resolution`，如果材料是基於目錄條目，否則， `attribute::Resolution`如果未 `res= is` 指定或設定為小於或等於0的值。

## 另請參閱 {#section-c00f6fb7b3e74719ac361de9a9ce4e52}

[材料解析度](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b),  [size=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-size.md#reference-1220d6fbcde4479aba91de7adacdc988),  [catalog::Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-resolution-dataref.md#reference-6a2d64c2d72b438fade58a3391569da7),  [attribute::Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
