---
title: CarouselView.frametransition
description: CarouselView.frametransition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 771395fb-775d-462e-86dc-0600cfecb345
source-git-commit: 5a7af31d6788ded908a5e1630a3b1b0723e6fb4b
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 4%

---

# CarouselView.frametransition{#carouselview-frametransition}

` [CarouselView.|<containerId>_carouselView.]frametransition=none|fade|slide[, *`持續時間`*[, *`間距`*]`

<table id="table_D5992FCFF26046079089652B211BB6C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 無|淡入|幻燈片 </span> </p> </td> 
   <td colname="col2"> <p>指定應用於幀更改的效果的類型。 比如說， <span class="codeph"> 無 </span> 代表沒有過渡；幀更改會立即發生。 還有， </p> <p> <span class="codeph"> 淡 </span> 表示舊幀和新幀之間的交叉漸隱轉換。 終於， </p> <p> <span class="codeph"> 滑 </span> 激活舊框架從視圖中滑出而新框架在其中滑入的過渡。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 持續時間 </span> </span> </p> </td> 
   <td colname="col2"> <p>指定的持續時間（秒） <span class="codeph"> 淡 </span> 或 <span class="codeph"> 滑 </span> 過渡效果。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 間距 </span> </span> </p> </td> 
   <td colname="col2"> <p>中相鄰幀之間的間距 <span class="codeph"> 滑 </span> 轉換，範圍為 <span class="codeph"> 0 </span> 通 <span class="codeph"> 1 </span> 與元件寬度有關。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

選擇性.

## 預設 {#section-71fb773f814649b2885aefee68073641}

無。

## 範例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`frametransition=fade,0.3`
