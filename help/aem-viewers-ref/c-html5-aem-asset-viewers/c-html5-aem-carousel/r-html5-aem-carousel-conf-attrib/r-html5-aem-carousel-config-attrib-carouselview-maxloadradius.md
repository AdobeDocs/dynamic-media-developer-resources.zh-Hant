---
description: CarouselView.maxloadradius
solution: Experience Manager
title: CarouselView.maxloadradius
feature: Dynamic Media經典，檢視器，SDK/API，轉盤橫幅
role: 開發人員，商業從業人員
exl-id: 8a3d3d32-7970-420c-8ad8-296c9ba1f08a
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 5%

---

# CarouselView.maxloadradius{#carouselview-maxloadradius}

` [CarouselView.|<containerId>_carouselView.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_B3B03B00DCF0466DB332E851F4DDF610"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> -1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td> <p>指定元件預載行為。 </p> <p>當設為<span class="codeph"> -1</span>時，元件將在空閒狀態下預先載入所有轉盤幀。 </p> <p>當設為<span class="codeph"> 0</span>時，元件僅載入目前可見、上一和下一幀的幀。 </p> <p><span class="codeph"><span class="varname"> preloadnbr</span></span>定義當處於空閒狀態時，預載當前顯示幀周圍的不可見幀數。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

選填。

## 預設 {#section-71fb773f814649b2885aefee68073641}

`1`

## 範例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`maxloadradius=0`
