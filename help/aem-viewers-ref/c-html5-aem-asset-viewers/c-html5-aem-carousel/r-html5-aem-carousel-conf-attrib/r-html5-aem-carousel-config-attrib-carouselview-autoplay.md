---
description: 轉盤檢視器的設定屬性。
solution: Experience Manager
title: CarouselView.autoplay
feature: Dynamic Media經典，檢視器，SDK/API，轉盤橫幅
role: 開發人員，商業從業人員
exl-id: 43b5c169-0ef6-4a12-a777-d36c1a8d1771
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 5%

---

# CarouselView.autoplay{#carouselview-autoplay}

轉盤檢視器的設定屬性。

`[CarouselView.|<containerId>_carouselView.]autoplay=[0|1][,duration][,direction]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">[0|1][,duration][,direction]</span> </p> </td> 
   <td colname="col2"> <p> 指定開／關、持續時間，以顯示浮動切換和自動循環方向中的每個橫幅。 </p> <p>設為<span class="codeph"> 0</span>以自動循環關閉。 </p> <p>將<span class="codeph"> 1</span>設為自動循環開啟，轉換持續時間以秒為單位，由<span class="codeph">持續時間</span>控制。 </p> <p>自動迴路的方向以<span class="codeph">方向</span>控制。 <span class="codeph">方向</span>具有從右至左的<span class="codeph">1</span>和從左至右的<span class="codeph">0</span>範圍。 </p> </td> 
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
