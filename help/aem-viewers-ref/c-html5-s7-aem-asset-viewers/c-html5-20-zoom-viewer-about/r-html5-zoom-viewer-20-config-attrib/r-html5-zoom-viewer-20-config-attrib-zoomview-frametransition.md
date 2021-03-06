---
title: ZoomView.frametransition
description: ZoomView.frametransition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: f57a8a2e-63a1-4a59-9a25-b435d0ac39dc
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 5%

---

# ZoomView.frametransition{#zoomview-frametransition}

` [ZoomView.|<containerId>_zoomView.]frametransition=none|fade|slide[, *`持續時間`*[, *`間距`*]`

<table id="table_D5992FCFF26046079089652B211BB6C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 無|淡化|幻燈片 </span> </p> </td> 
   <td colname="col2"> <p>指定對幀更改應用的效果類型。 屬性 <span class="codeph"> 無 </span> 代表不轉變；框架變化會立即發生。 屬性 <span class="codeph"> 淡出 </span> 表示舊幀和新幀之間的交叉淡出過渡。 屬性 <span class="codeph"> 幻燈片 </span> 激活舊框架滑出視圖而新框架滑入的過渡。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 持續時間 </span> </span> </p> </td> 
   <td colname="col2"> <p>指定的持續時間（以秒為單位） <span class="codeph"> 淡出 </span> 或 <span class="codeph"> 幻燈片 </span> 過渡效果。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 間距 </span> </span> </p> </td> 
   <td colname="col2"> <p>中相鄰幀之間的間距 <span class="codeph"> 幻燈片 </span> 轉變，範圍為 <span class="codeph"> 0 </span> through <span class="codeph"> 1 </span> 和是相對於元件寬度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

選填。

## 預設 {#section-71fb773f814649b2885aefee68073641}

無。

## 範例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`frametransition=fade,1`
