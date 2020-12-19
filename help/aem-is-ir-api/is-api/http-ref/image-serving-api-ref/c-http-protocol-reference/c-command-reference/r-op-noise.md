---
description: 加入雜訊。 將隨機雜訊加入前景影像資料或效果圖層的前景。
seo-description: 加入雜訊。 將隨機雜訊加入前景影像資料或效果圖層的前景。
seo-title: op_noise
solution: Experience Manager
title: op_noise
topic: Scene7 Image Serving - Image Rendering API
uuid: 531f7a94-149b-4090-a163-a1895156250b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 1%

---


# op_noise{#op-noise}

加入雜訊。 將隨機雜訊加入前景影像資料或效果圖層的前景。

`op_noise= *`彩色`*[,uniform|gaussian[, *`單色`*]]`

<table id="table_40675464E5824D52BF392ECCE2DDC03C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> val</span> </p> </td> 
   <td colname="col2"> <p>雜訊量（百分比）(0...100 int)。 </p> </td> 
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
   <td colname="col2"> <p>對於顏色雜訊，設為0，對於灰色雜訊，設為1。 </p> </td> 
  </tr> 
 </tbody> 
</table>

*`monochrome`* 的值。

## 屬性 {#section-1f1a64c791f545a3bf1abd0b0e575d87}

圖層命令。 如果`layer=comp`，則套用至目前圖層或複合影像。

## 預設 {#section-d548868fa4b64a60bcb481cad1f8113e}

`op_noise=0,uniform,0`，免得發出噪音。
