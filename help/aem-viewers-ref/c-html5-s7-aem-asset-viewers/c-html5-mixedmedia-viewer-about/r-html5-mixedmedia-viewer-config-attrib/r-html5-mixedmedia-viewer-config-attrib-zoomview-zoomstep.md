---
title: ZoomView.zoomstep
description: ZoomView.zoomstep
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 5d978d21-7942-4bd6-b742-9bf4b6fd3ebe
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 7%

---

# ZoomView.zoomstep{#zoomview-zoomstep}

` [ZoomView.|<containerId>_zoomView.]zoomstep= *`步`*[, *`限`*]`

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 步驟</span></span> </p> </td> 
   <td colname="col2"> <p> 配置將解析度提高或降低2倍所需的數字放大和縮小操作。 每個縮放操作的解析度變化是每步2^1。 設定為 <span class="codeph"> 0</span> 以使用單個縮放操作縮放到完全解析度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 限制</span></span> </p> </td> 
   <td colname="col2"> <p> 指定相對於全解析度影像的最大縮放解析度。 預設值為 <span class="codeph"> 1.0</span>，這不允許超出全解析度的縮放。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

選填。

## 預設 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1,1`

## 範例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`zoomstep=2,3`
