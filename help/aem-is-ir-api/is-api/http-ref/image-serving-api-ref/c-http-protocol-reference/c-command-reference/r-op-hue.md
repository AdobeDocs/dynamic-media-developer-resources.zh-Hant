---
description: 調整色相。 將圖層或合成影像的每個可見像素的色相依指定量移動。
seo-description: 調整色相。 將圖層或合成影像的每個可見像素的色相依指定量移動。
seo-title: op_hue
solution: Experience Manager
title: op_hue
uuid: 23da539e-0192-4dc4-a19b-41aa94a82730
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 1%

---


# op_hue{#op-hue}

調整色相。 將圖層或合成影像的每個可見像素的色相依指定量移動。

`op_hue= *`adj`*`

<table id="simpletable_7DC7ABA384664BDDAA65B8DEEF7859A8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>度調整的色相(-180...+180 int)。 </p></td> 
 </tr> 
</table>

根據360度的色相範圍。

## 屬性 {#section-55779644700b4c808a624cdf5a04447e}

圖層命令。 如果`layer=comp`，則套用至目前圖層或複合影像。 被效果圖層忽略。 在應用操作之前，CMYK影像或圖層將轉換為RGB。

## 預設 {#section-7314580251f5456fa1f381ec9e99e0bb}

`op_hue=0`，以取得色調不變的效果。
