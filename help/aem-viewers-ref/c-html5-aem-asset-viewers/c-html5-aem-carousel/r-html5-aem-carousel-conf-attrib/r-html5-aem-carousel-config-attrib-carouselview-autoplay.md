---
description: 轉盤檢視器的設定屬性。
seo-description: 轉盤檢視器的設定屬性。
seo-title: CarouselView.autoplay
solution: Experience Manager
title: CarouselView.autoplay
topic: Dynamic media
uuid: 12730b17-110e-405b-97fe-e70fab89c703
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# CarouselView.autoplay{#carouselview-autoplay}

轉盤檢視器的設定屬性。

`[CarouselView.|<containerId>_carouselView.]autoplay=[0|1][,duration][,direction]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">[0|1][,duration][,direction]</span> </p> </td> 
   <td colname="col2"> <p> 指定開／關、持續時間，以顯示浮動切換和自動循環方向中的每個橫幅。 </p> <p>設為 <span class="codeph"> 0</span> ，自動循環關閉。 </p> <p>將 <span class="codeph"> 1設為</span> 「自動循環開啟」，轉場持續時間（以秒為單位）由持續時間 <span class="codeph"> 控制</span>。 </p> <p>自動迴路的方向由方向控 <span class="codeph"> 制</span>。 方 <span class="codeph"> 向</span> ，範圍為 <span class="codeph"> 1</span> -右——左至 <span class="codeph"> 0</span> -左——右。 </p> </td> 
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

