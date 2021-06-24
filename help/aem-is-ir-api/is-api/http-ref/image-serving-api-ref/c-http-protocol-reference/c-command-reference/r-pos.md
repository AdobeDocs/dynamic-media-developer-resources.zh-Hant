---
description: 圖層位置。
solution: Experience Manager
title: pos
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: c2e9a1f3-7216-4ab0-9c37-57f083119cef
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 3%

---

# pos{#pos}

圖層位置。

pos= *`coord`*

posN= *`coordN`*

<table id="simpletable_754F76EE00BF4129B07502647FF172B7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 坐標</span> </p> </td> 
  <td class="stentry"> <p>從此層原點到0層原點(int、int)的像素偏移。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coordN</span> </p></td> 
  <td class="stentry"> <p>從此層的原點到0層原點的歸一化偏移（實數、實數）。 </p></td> 
 </tr> 
</table>

對於影像、文本和實色層，`pos=`指定層錨點相對於層0錨點的位置。 `posN=` 坐標值相對於實際層0直接大小進行歸一化。

在效果層中，`pos=`將效果層相對於父層移動。

正值會將圖層向右/向下移動，向左/向上移動。 `posN=0.5,0.5` 將圖層0的寬度和高度的一半向下和向右移動。

## 屬性 {#section-51a60cdc52d040538fef378ace7c2e7d}

層屬性。 若`layer=0`或`layer=comp`，則忽略。

## 預設 {#section-70a6bc71ded5494e843194dfb6bf5a6c}

`posN=0,0`. 如果圖層是影像、文本或實色圖層，則將圖層錨點置於與圖層0錨點相同的位置。 將效果層直接置於其父層之上或之下。

## 範例 {#section-a89a02c22f6b4260bfcf7c842cd6069d}

請參閱[範本](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)中的範例A。

## 另請參閱 {#section-812d95575ba542808e8387d0a8650606}

[origin=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138)
