---
description: 物質解析度。 指定可重複紋理或貼圖影像的解析度。
solution: Experience Manager
title: res
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 3%

---


# res{#res}

物質解析度。 指定可重複紋理或貼圖影像的解析度。

` res= *`val`*`

<table id="simpletable_2004B804D46E43C090E59BBFF8144598"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val  </span> </p> </td> 
  <td class="stentry"> <p>決議；材質解析度單位（通常是每英吋像素）（實數）。 </p> </td> 
 </tr> 
</table>

對於傾斜材料，如果同時指定`size=`和`res=`，則`size=`佔優。

## 屬性 {#section-6a458ddc202f46e0b668c9f040a65cef}

材料屬性。 被純色材料忽略。 只有在使用紋理時，才能通過機櫃和窗口覆蓋材料。

## 預設 {#section-ee4088a994014df59105fc1dbb2aa042}

`catalog::Resolution`，如果材料基於目錄條目，則 `attribute::Resolution`否，如 `res= is` 果未指定或設定為小於或等於0。

## 另請參閱 {#section-c00f6fb7b3e74719ac361de9a9ce4e52}

[Material Resolution](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b),  [size=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-size.md#reference-1220d6fbcde4479aba91de7adacdc988), catalog::Resolution [, ](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-resolution-dataref.md#reference-6a2d64c2d72b438fade58a3391569da7) [attribute::Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
