---
description: 圖層位置。
solution: Experience Manager
title: pos
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c2e9a1f3-7216-4ab0-9c37-57f083119cef
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 2%

---

# pos{#pos}

圖層位置。

pos= *`coord`*

posN= *`coordN`*

<table id="simpletable_754F76EE00BF4129B07502647FF172B7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 坐標</span> </p> </td> 
  <td class="stentry"> <p>從此層原點到層0原點(int, int)的像素偏移。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 坐標N</span> </p></td> 
  <td class="stentry"> <p>從此層原點到層0原點的歸一化偏移（實數、實數）。 </p></td> 
 </tr> 
</table>

對於影像、文本和純色圖層， `pos=` 指定圖層錨點相對於圖層0錨點的位置。 `posN=` 坐標值相對於實際層0直接大小進行歸一化。

如果是效果層， `pos=` 相對於父層移動效果層。

正值將圖層向右/下移動，向左/上移動負值。 `posN=0.5,0.5` 將圖層向下和向右移動圖層0寬度和高度的一半。

## 屬性 {#section-51a60cdc52d040538fef378ace7c2e7d}

層屬性。 如果忽略 `layer=0` 或 `layer=comp`。

## 預設 {#section-70a6bc71ded5494e843194dfb6bf5a6c}

`posN=0,0`. 如果圖層是影像、文本或純色圖層，則會將圖層錨點置於與圖層0錨點相同的位置。 將效果圖層直接置於其父圖層上或下。

## 範例 {#section-a89a02c22f6b4260bfcf7c842cd6069d}

請參閱中的示例A [模板](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)。

## 另請參閱 {#section-812d95575ba542808e8387d0a8650606}

[原產地=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138)
