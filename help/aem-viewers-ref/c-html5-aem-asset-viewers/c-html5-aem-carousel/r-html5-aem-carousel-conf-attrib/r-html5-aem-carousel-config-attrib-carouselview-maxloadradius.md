---
description: CarouselView.maxloadradius
solution: Experience Manager
title: CarouselView.maxloadradius
feature: Dynamic Media Classic，檢視器，SDK/API，輪播橫幅
role: Developer,User
exl-id: 8a3d3d32-7970-420c-8ad8-296c9ba1f08a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 5%

---

# CarouselView.maxloadradius{#carouselview-maxloadradius}

` [CarouselView.|<containerId>_carouselView.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_B3B03B00DCF0466DB332E851F4DDF610"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> -1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td> <p>指定元件預載行為。 </p> <p>當設定為<span class="codeph"> -1</span>時，元件將在空閒狀態下預載入所有輪播幀。 </p> <p>當設定為<span class="codeph"> 0</span>時，元件僅載入當前可見、前一幀和下一幀的幀。 </p> <p><span class="codeph"><span class="varname"> </span></span>preloadnbr定義了當處於空閒狀態時，在當前顯示的幀周圍預載入的不可見幀數。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

選填。

## 預設 {#section-71fb773f814649b2885aefee68073641}

`1`

## 範例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`maxloadradius=0`
