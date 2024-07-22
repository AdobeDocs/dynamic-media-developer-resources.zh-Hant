---
title: op_noise
description: 加入雜訊。 將隨機雜訊加入前景影像資料中，或加入效果圖層的前景中。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: eeadd3ab-80ff-4f9b-b5b7-4f3da6feebde
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 1%

---

# op_noise{#op-noise}

加入雜訊。 將隨機雜訊加入前景影像資料中，或加入效果圖層的前景中。

`op_noise= *`val`*[,uniform|gaussian[, *`單色`*]]`

<table id="table_40675464E5824D52BF392ECCE2DDC03C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">值</span> </p> </td> 
   <td colname="col2"> <p>雜訊量，以百分比表示(0...100 int)。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">統一</span> </p> </td> 
   <td colname="col2"> <p>選取均勻雜訊分佈。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">高斯</span> </p> </td> 
   <td colname="col2"> <p>選取高斯雜訊分佈。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname">單色</span> </p> </td> 
   <td colname="col2"> <p>設定為0代表色彩雜訊，設為1代表灰色雜訊。 </p> </td> 
  </tr> 
 </tbody> 
</table>

已忽略灰階影像的&#x200B;*`monochrome`*。

## 屬性 {#section-1f1a64c791f545a3bf1abd0b0e575d87}

圖層指令。 套用至目前的圖層或複合影像（若為`layer=comp`）。

## 預設 {#section-d548868fa4b64a60bcb481cad1f8113e}

`op_noise=0,uniform,0`，無雜訊。
