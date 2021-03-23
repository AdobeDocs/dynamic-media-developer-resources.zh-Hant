---
description: ZoomView.zoomstep
solution: Experience Manager
title: ZoomView.zoomstep
uuid: 948b154a-250c-41a8-967b-d199ddb6e5e1
feature: Dynamic Media經典，檢視器，SDK/API，縮放
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 4%

---


# ZoomView.zoomstep{#zoomview-zoomstep}

` [ZoomView.|<containerId>_zoomView.]zoomstep= *``*[, *`Steplimit`*]`

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 步驟</span> </span> </p> </td> 
   <td colname="col2"> <p> 配置將解析度提高或降低兩倍所需的放大和縮小操作數。 每個縮放動作的解析度變更是每個步驟2^1。 設為<span class="codeph"> 0</span>，只要單一縮放動作，即可縮放至完整解析度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 限制</span> </span> </p> </td> 
   <td colname="col2"> <p> 指定相對於完整解析度影像的最大縮放解析度。 預設值為<span class="codeph"> 1.0</span>，不允許縮放超過完整解析度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-50bcd15223174bb79ce08b31ea03d682}

選填。

## 預設 {#section-7564169749ff4a4996049ea1148cb2a5}

`1,1`

## 範例 {#section-96e69b70365f461dae4399e49044ea2f}

`zoomstep=2,3`
