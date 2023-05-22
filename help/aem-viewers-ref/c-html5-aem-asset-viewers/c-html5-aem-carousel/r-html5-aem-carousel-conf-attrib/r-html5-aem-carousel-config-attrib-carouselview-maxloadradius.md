---
title: CarouselView.maxloadradius
description: CarouselView.maxloadradius
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 8a3d3d32-7970-420c-8ad8-296c9ba1f08a
source-git-commit: 5a7af31d6788ded908a5e1630a3b1b0723e6fb4b
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 4%

---

# CarouselView.maxloadradius{#carouselview-maxloadradius}

` [CarouselView.|<containerId>_carouselView.]maxloadradius=-1|0| *`預載入br`*`

<table id="table_B3B03B00DCF0466DB332E851F4DDF610"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> -1|0|<span class="varname"> 預載入br</span></span> </p> </td> 
   <td> <p>指定元件預載入行為。 </p> <p>設定為時 <span class="codeph"> -1</span> 當元件處於空閒狀態時，該元件將預載所有旋轉軸框架。 </p> <p>設定為時 <span class="codeph"> 0</span> 該元件僅載入當前可見的幀、上一幀和下一幀。 </p> <p><span class="codeph"><span class="varname"> 預載入br</span></span>定義當當前顯示的幀周圍處於空閒狀態時預載入的不可見幀的數量。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

選擇性.

## 預設 {#section-71fb773f814649b2885aefee68073641}

`1`

## 範例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`maxloadradius=0`
