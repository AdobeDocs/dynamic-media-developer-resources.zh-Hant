---
description: 輪播檢視器的設定屬性。
solution: Experience Manager
title: CarouselView.autoplay
feature: Dynamic Media Classic，檢視器，SDK/API，輪播橫幅
role: Developer,User
exl-id: 43b5c169-0ef6-4a12-a777-d36c1a8d1771
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 5%

---

# CarouselView.autoplay{#carouselview-autoplay}

輪播檢視器的設定屬性。

`[CarouselView.|<containerId>_carouselView.]autoplay=[0|1][,duration][,direction]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">[0|1][,duration][,direction]</span> </p> </td> 
   <td colname="col2"> <p> 指定開啟/關閉、在輪播中顯示每個橫幅的持續時間以及自動循環的方向。 </p> <p>設為<span class="codeph"> 0</span>以自動關閉循環。 </p> <p>將<span class="codeph"> 1</span>設為自動循環開啟，轉換持續時間以秒為單位，由<span class="codeph">持續時間</span>控制。 </p> <p>自動迴路的方向以<span class="codeph">方向</span>控制。 <span class="codeph">方向</span>的範圍介於<span class="codeph"> 1</span>從右到左和<span class="codeph"> 0</span>從左到右之間。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

選填。

## 預設 {#section-71fb773f814649b2885aefee68073641}

`1,9`

## 範例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
autoplay=1,2,1
```
