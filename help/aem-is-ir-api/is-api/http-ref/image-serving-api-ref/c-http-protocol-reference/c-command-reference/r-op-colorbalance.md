---
description: 調整顏色平衡。 分別調整每個RGB顏色分量的值。
solution: Experience Manager
title: op_colorbalance
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 93476778-97b0-4ad5-b22a-093239e845f0
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 2%

---

# op_colorbalance{#op-colorbalance}

調整顏色平衡。 分別調整每個RGB顏色分量的值。

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

灰度和CMYK輸入影像資料使用天基轉換轉換為RGB，當啟用顏色管理時，這種轉換不準確。

## 屬性 {#section-dff9c934f7c1442bbd02379b688d82e2}

圖層命令。 若`layer=comp`，則套用至目前層或複合影像。 被效果層忽略。 在應用操作之前， CMYK影像和圖層會轉換為RGB。

## 預設 {#section-08d84ef715964f7daea86f5ef237d199}

`op_colorbalance=0,0,0` 不換顏色。

## 範例 {#section-7e97fa36e01d4af8ab03fc9d493da1a1}

將顏色平衡推向紅色：

… `&op_colorBalance=100,0,0&`…
