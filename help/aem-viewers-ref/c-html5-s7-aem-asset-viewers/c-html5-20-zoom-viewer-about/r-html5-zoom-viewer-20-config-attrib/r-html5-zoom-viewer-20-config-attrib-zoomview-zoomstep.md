---
description: ZoomView.zoomstep
solution: Experience Manager
title: ZoomView.zoomstep
feature: Dynamic Media Classic，檢視器，SDK/API，縮放
role: Developer,User
exl-id: bcd153f3-7a87-4e8f-825b-fc4a136de1dc
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 7%

---

# ZoomView.zoomstep{#zoomview-zoomstep}

` [ZoomView.|<containerId>_zoomView.]zoomstep= *``*[, *`steplimit`*]`

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 步驟</span></span> </p> </td> 
   <td colname="col2"> <p> 配置將解析度增加或降低2倍所需的操作放大和縮小。 每個縮放動作的解析度變化為每步驟2^1。 設為<span class="codeph"> 0</span> ，只要執行一次縮放動作即可縮放至完整解析度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 限制</span></span> </p> </td> 
   <td colname="col2"> <p> 指定相對於完整解析度影像的最大縮放解析度。 預設值為<span class="codeph"> 1.0</span>，不允許縮放超過完全解析度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

選填。

## 預設 {#section-71fb773f814649b2885aefee68073641}

`1,1`

## 範例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`zoomstep=2,3`
