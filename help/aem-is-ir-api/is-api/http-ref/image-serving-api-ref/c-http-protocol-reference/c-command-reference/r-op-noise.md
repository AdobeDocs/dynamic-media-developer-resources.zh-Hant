---
description: 添加噪音。 將隨機雜訊添加到前景影像資料或效果層的前景。
solution: Experience Manager
title: op_noise
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: eeadd3ab-80ff-4f9b-b5b7-4f3da6feebde
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 1%

---

# op_noise{#op-noise}

添加噪音。 將隨機雜訊添加到前景影像資料或效果層的前景。

`op_noise= *`谷`*[,uniform|gaussian[, *`單色`*]]`

<table id="table_40675464E5824D52BF392ECCE2DDC03C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 谷</span> </p> </td> 
   <td colname="col2"> <p>雜訊量（百分比）(0...100 int)。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 均勻</span> </p> </td> 
   <td colname="col2"> <p>選擇均勻雜訊分佈。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 高斯</span> </p> </td> 
   <td colname="col2"> <p>選擇高斯雜訊分佈。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 單色</span> </p> </td> 
   <td colname="col2"> <p>對於顏色噪音，設定為0；對於灰色噪音，設定為1。 </p> </td> 
  </tr> 
 </tbody> 
</table>

*`monochrome`* 忽略灰度影像。

## 屬性 {#section-1f1a64c791f545a3bf1abd0b0e575d87}

層命令。 應用於當前圖層或複合影像 `layer=comp`。

## 預設 {#section-d548868fa4b64a60bcb481cad1f8113e}

`op_noise=0,uniform,0`，無噪音。
