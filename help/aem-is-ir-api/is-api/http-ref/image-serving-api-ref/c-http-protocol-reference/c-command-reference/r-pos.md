---
description: 圖層位置。
solution: Experience Manager
title: pos
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 3%

---


# pos{#pos}

圖層位置。

pos= *`coord`*

posN= *`coordN`*

<table id="simpletable_754F76EE00BF4129B07502647FF172B7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 坐標</span> </p> </td> 
  <td class="stentry"> <p>像素從此圖層的原點偏移到圖層0原點(int, int)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coordN</span> </p></td> 
  <td class="stentry"> <p>從此圖層原點到圖層0原點的標準化偏移（實數、實數）。 </p></td> 
 </tr> 
</table>

對於影像、文本和純色圖層，`pos=`指定圖層錨點相對於圖層0錨點的位置。 `posN=` 坐標值相對於實際的0層直接大小進行標準化。

在特效圖層的情況下，`pos=`會相對於父層移動特效圖層。

正值會將圖層朝右／下方移動，向左／上方移動負值。 `posN=0.5,0.5` 將圖層0的寬度和高度向下和向右移動一半。

## 屬性 {#section-51a60cdc52d040538fef378ace7c2e7d}

層屬性。 如果`layer=0`或`layer=comp`，則忽略。

## 預設 {#section-70a6bc71ded5494e843194dfb6bf5a6c}

`posN=0,0`. 如果圖層錨點是影像、文字或純色圖層，則會將圖層錨點置於圖層0錨點的相同位置。 將效果圖層直接置於其父圖層上或下。

## 範例 {#section-a89a02c22f6b4260bfcf7c842cd6069d}

請參閱[Templates](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)中的範例A。

## 另請參閱 {#section-812d95575ba542808e8387d0a8650606}

[原點=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138)
