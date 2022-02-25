---
title: ZoomView.zoomstep
description: ZoomView.zoomstep
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: ded8168e-08f7-4bc0-bb8a-624bac82759e
source-git-commit: 7eddc50fb9803eacdd1f513c6132380793b6f88d
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 5%

---

# ZoomView.zoomstep{#zoomview-zoomstep}

` [ZoomView.|<containerId>_zoomView.]zoomstep= *`步`*[, *`限`*]`

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 步</span> </span> </p> </td> 
   <td colname="col2"> <p> 配置將解析度提高或降低兩倍所需的放大和縮小操作數。 每個縮放操作的解析度變化是每步2^1。 設定為 <span class="codeph"> 0</span> 以使用單個縮放操作縮放到完全解析度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 限</span> </span> </p> </td> 
   <td colname="col2"> <p> 指定相對於全解析度影像的最大縮放解析度。 預設值為 <span class="codeph"> 1.0</span>，這不允許超出全解析度的縮放。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-50bcd15223174bb79ce08b31ea03d682}

選填。

## 預設 {#section-7564169749ff4a4996049ea1148cb2a5}

`1,1`

## 範例 {#section-96e69b70365f461dae4399e49044ea2f}

`zoomstep=2,3`
