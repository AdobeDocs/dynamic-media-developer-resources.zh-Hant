---
title: op_hue
description: 調整影像色相。 將圖層或複合影像的每個可見畫素的色相位移指定的數量。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b436bd31-12a9-42ed-9ad3-5ff91e3ccce9
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 1%

---

# op_hue{#op-hue}

調整影像色相。 將圖層或複合影像的每個可見畫素的色相位移指定的數量。

`op_hue= *`adj`*`

<table id="simpletable_7DC7ABA384664BDDAA65B8DEEF7859A8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname">調整</span> </p> </td> 
  <td class="stentry"> <p>色相調整，以度為單位(-180...+180 int)。 </p></td> 
 </tr> 
</table>

以360度的色相範圍為基礎。

## 屬性 {#section-55779644700b4c808a624cdf5a04447e}

圖層指令。 套用至目前的圖層或複合影像（若為`layer=comp`）。 被效果圖層忽略。 CMYK影像或圖層會在套用作業之前轉換為RGB。

## 預設 {#section-7314580251f5456fa1f381ec9e99e0bb}

`op_hue=0`，無色相變更。
