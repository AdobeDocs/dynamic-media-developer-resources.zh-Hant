---
description: CarouselView.enableHD
solution: Experience Manager
title: CarouselView.enableHD
feature: Dynamic Media Classic，檢視器，SDK/API，輪播橫幅
role: Developer,User
exl-id: c94ac151-3115-42ac-8a76-13b8769293cb
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 6%

---

# CarouselView.enableHD{#carouselview-enablehd}

` [CarouselView.|<containerId>_carouselView.]enableHD=always|never|limit[, *`數字`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 一律|從不|限制</span> </p> </td> 
   <td colname="col2"> <p> 對<span class="codeph"> devicePixelRatio</span>大於<span class="codeph"> 1</span>的設備啟用、限制或禁用優化，即具有高密度顯示的設備，如iPhone4和類似設備。 </p> <p>如果活動，則元件將限制IS影像請求的大小，就像設備只有<span class="codeph"> 1</span>的像素比，這樣可以減少頻寬。 </p> <p>請參閱下列範例。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 數字</span></span> </p> </td> 
   <td colname="col2"> <p> 如果使用<span class="codeph"> limit</span>設定，則元件僅啟用高像素密度，而達到指定的限制。 </p> <p>請參閱下列範例。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

選填。

## 預設 {#section-71fb773f814649b2885aefee68073641}

`limit,1500`

## 範例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`enableHD=always`
