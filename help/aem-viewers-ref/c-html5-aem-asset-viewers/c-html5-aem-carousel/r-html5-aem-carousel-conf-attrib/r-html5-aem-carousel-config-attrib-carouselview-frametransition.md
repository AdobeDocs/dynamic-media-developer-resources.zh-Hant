---
description: CarouselView.frametransition
solution: Experience Manager
title: CarouselView.frametransition
uuid: 9539ede1-08fb-4bfc-8a5a-870c7d84de7f
feature: Dynamic Media經典，檢視器，SDK/API，轉盤橫幅
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 4%

---


# CarouselView.frametransition{#carouselview-frametransition}

` [CarouselView.|<containerId>_carouselView.]frametransition=none|fade|slide[, *`持續`*[, *`間距`*]`

<table id="table_D5992FCFF26046079089652B211BB6C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade|slide  </span> </p> </td> 
   <td colname="col2"> <p>指定影格變更所套用之效果的類型。 <span class="codeph"> 沒 </span> 有代表不轉變；影格變更會立即發生。 </p> <p> <span class="codeph"> 淡 </span> 出表示新舊影格之間的交叉淡出轉換。 </p> <p> <span class="codeph"> slide </span> 會啟動轉場，讓舊影格滑出檢視，而新影格滑入。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 持續時間  </span> </span> </p> </td> 
   <td colname="col2"> <p>指定<span class="codeph">淡化</span>或<span class="codeph">投影片</span>過渡效果的持續時間（以秒為單位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 間距  </span> </span> </p> </td> 
   <td colname="col2"> <p>在<span class="codeph">幻燈片</span>過渡中相鄰幀之間的間距在<span class="codeph"> 0 </span>和<span class="codeph"> 1 </span>之間，且與元件寬度相關。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

選填。

## 預設 {#section-71fb773f814649b2885aefee68073641}

無。

## 範例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`frametransition=fade,0.3`
