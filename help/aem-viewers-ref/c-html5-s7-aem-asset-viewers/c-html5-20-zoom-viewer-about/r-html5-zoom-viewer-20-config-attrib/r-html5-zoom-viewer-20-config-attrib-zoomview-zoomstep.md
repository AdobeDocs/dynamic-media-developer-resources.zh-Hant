---
description: ZoomView.zoomstep
solution: Experience Manager
title: ZoomView.zoomstep
topic: Dynamic media
uuid: bc68fc0a-94bf-42b3-a386-e0a248e8445c
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 7%

---


# ZoomView.zoomstep{#zoomview-zoomstep}

` [ZoomView.|<containerId>_zoomView.]zoomstep= *``*[, *`Steplimit`*]`

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 步驟</span></span> </p> </td> 
   <td colname="col2"> <p> 配置將解析度提高或降低2倍所需的縮放和縮小操作數。 每個縮放動作的解析度變更是每個步驟2^1。 設為<span class="codeph"> 0</span>，只要單一縮放動作，即可縮放至完整解析度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 限制</span></span> </p> </td> 
   <td colname="col2"> <p> 指定相對於完整解析度影像的最大縮放解析度。 預設值為<span class="codeph"> 1.0</span>，不允許縮放超過完整解析度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

選填。

## 預設 {#section-71fb773f814649b2885aefee68073641}

`1,1`

## 範例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`zoomstep=2,3`
