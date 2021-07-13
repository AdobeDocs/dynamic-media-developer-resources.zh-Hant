---
description: 調整色相。 將圖層或複合影像的每個可見像素的色相按指定量進行移位。
solution: Experience Manager
title: op_hue
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b436bd31-12a9-42ed-9ad3-5ff91e3ccce9
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 2%

---

# op_hue{#op-hue}

調整色相。 將圖層或複合影像的每個可見像素的色相按指定量進行移位。

`op_hue= *`adj`*`

<table id="simpletable_7DC7ABA384664BDDAA65B8DEEF7859A8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>度的色相調整(-180...+180 int)。 </p></td> 
 </tr> 
</table>

基於360度的色調範圍。

## 屬性 {#section-55779644700b4c808a624cdf5a04447e}

圖層命令。 若`layer=comp`，則套用至目前層或複合影像。 被效果層忽略。 在應用操作之前， CMYK影像或圖層會轉換為RGB。

## 預設 {#section-7314580251f5456fa1f381ec9e99e0bb}

`op_hue=0`，不會變更色相。
