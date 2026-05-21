---
title: ZoomView.zoomstep
description: ZoomView.zoomstep
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: ded8168e-08f7-4bc0-bb8a-624bac82759e
TQID: 'https://experienceleague.adobe.com/hJGTnjDC-x9P3Q0vbq0mXuumwtZHAVfxcVWPXkemyoI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 82
ht-degree: 3%

---

# ZoomView.zoomstep{#zoomview-zoomstep}

` [ZoomView.|<containerId>_zoomView.]zoomstep= *`步驟`*[, *`限制`*]`

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">步驟</span> </span> </p> </td> 
   <td colname="col2"> <p> 設定以2的係數增加或減少解析度所需的放大和縮小動作數目。 每個縮放動作的解析度變化是每步階2^1。 設定為<span class="codeph"> 0</span>以使用單一縮放動作縮放至完整解析度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">限制</span> </span> </p> </td> 
   <td colname="col2"> <p> 指定相對於完整解析度影像的最大縮放解析度。 預設值為<span class="codeph"> 1.0</span>，不允許縮放超過完整解析度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-50bcd15223174bb79ce08b31ea03d682}

選擇性.

## 預設 {#section-7564169749ff4a4996049ea1148cb2a5}

`1,1`

## 範例 {#section-96e69b70365f461dae4399e49044ea2f}

`zoomstep=2,3`
