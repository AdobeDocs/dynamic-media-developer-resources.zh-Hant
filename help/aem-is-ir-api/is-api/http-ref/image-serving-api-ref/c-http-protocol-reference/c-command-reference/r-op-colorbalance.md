---
description: 調整色彩平衡。 分別調整每個RGB顏色分量的值。
seo-description: 調整色彩平衡。 分別調整每個RGB顏色分量的值。
seo-title: op_colorbalance
solution: Experience Manager
title: op_colorbalance
topic: Scene7 Image Serving - Image Rendering API
uuid: 177aa6e3-1b32-4254-85f1-d7fe14116e3c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# op_colorbalance{#op-colorbalance}

調整色彩平衡。 分別調整每個RGB顏色分量的值。

`op_colorbalance= *``*, *``*, *`redAdjgreenAdjblueAdj`*`

<table id="simpletable_BBDAA6FE9A0E48E3BD8304BDED776713"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> redAdj</span> </p></td> 
  <td class="stentry"> <p>紅色元件調整(-100...+100 int)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> greenAdj</span> </p></td> 
  <td class="stentry"> <p>綠色元件調整(-100...+100 int)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> blueAdj</span> </p></td> 
  <td class="stentry"> <p>藍色元件調整(-100...+100 int)。 </p></td> 
 </tr> 
</table>

灰階和CMYK輸入影像資料會使用幼稚轉換來轉換為RGB，當啟用色彩管理時，這種轉換不準確。

## 屬性 {#section-dff9c934f7c1442bbd02379b688d82e2}

圖層命令。 應用於當前圖層或複合影像（如果） `layer=comp`。 被效果圖層忽略。 在應用操作之前，CMYK影像和圖層將轉換為RGB。

## 預設 {#section-08d84ef715964f7daea86f5ef237d199}

`op_colorbalance=0,0,0` 不能改變顏色。

## 範例 {#section-7e97fa36e01d4af8ab03fc9d493da1a1}

將色彩平衡推向紅色：

… `&op_colorBalance=100,0,0&`…
