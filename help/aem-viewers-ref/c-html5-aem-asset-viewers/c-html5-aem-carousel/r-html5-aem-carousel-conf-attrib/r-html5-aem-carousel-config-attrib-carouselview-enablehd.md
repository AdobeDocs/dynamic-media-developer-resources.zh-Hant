---
title: CarouselView.enableHD
description: CarouselView.enableHD
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: c94ac151-3115-42ac-8a76-13b8769293cb
source-git-commit: 5a7af31d6788ded908a5e1630a3b1b0723e6fb4b
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 5%

---

# CarouselView.enableHD{#carouselview-enablehd}

` [CarouselView.|<containerId>_carouselView.]enableHD=always|never|limit[, *`數字`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 始終|never|limit</span> </p> </td> 
   <td colname="col2"> <p> 對以下設備啟用、限制或禁用優化 <span class="codeph"> 設備PixelRatio</span> 大於 <span class="codeph"> 1</span>這就是像iPhone4和類似的器件一樣，具有高密度顯示的器件。 </p> <p>如果處於活動狀態，則元件將限制IS影像請求的大小，就好像設備僅具有像素比 <span class="codeph"> 1</span> 減少頻寬。 </p> <p>請參見下例。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 數字</span></span> </p> </td> 
   <td colname="col2"> <p> 如果使用 <span class="codeph"> 限</span> 設定時，該元件僅允許高像素密度達到指定限制。 </p> <p>請參見下例。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

選擇性.

## 預設 {#section-71fb773f814649b2885aefee68073641}

`limit,1500`

## 範例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`enableHD=always`
