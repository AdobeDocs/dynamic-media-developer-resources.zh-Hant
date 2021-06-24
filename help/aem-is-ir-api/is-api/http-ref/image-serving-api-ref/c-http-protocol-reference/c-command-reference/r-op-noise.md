---
description: 加噪音。 將隨機雜訊加到前景影像資料或效果層的前景。
solution: Experience Manager
title: op_noise
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: eeadd3ab-80ff-4f9b-b5b7-4f3da6feebde
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 2%

---

# op_noise{#op-noise}

加噪音。 將隨機雜訊加到前景影像資料或效果層的前景。

`op_noise= *``*[,uniform|gaussian[, *`彩色`*]]`

<table id="table_40675464E5824D52BF392ECCE2DDC03C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> val</span> </p> </td> 
   <td colname="col2"> <p>雜訊百分比(0...100 int)。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 均勻</span> </p> </td> 
   <td colname="col2"> <p>選擇均勻的雜訊分佈。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 高斯</span> </p> </td> 
   <td colname="col2"> <p>選擇高斯雜訊分佈。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 單色</span> </p> </td> 
   <td colname="col2"> <p>顏色雜訊設為0，灰色雜訊為1。 </p> </td> 
  </tr> 
 </tbody> 
</table>

*`monochrome`* 會忽略灰度影像。

## 屬性 {#section-1f1a64c791f545a3bf1abd0b0e575d87}

圖層命令。 若`layer=comp`，則套用至目前層或複合影像。

## 預設 {#section-d548868fa4b64a60bcb481cad1f8113e}

`op_noise=0,uniform,0`，無噪音。
