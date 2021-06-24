---
description: CarouselView.frametransition
solution: Experience Manager
title: CarouselView.frametransition
feature: Dynamic Media Classic，檢視器，SDK/API，輪播橫幅
role: Developer,Business Practitioner
exl-id: 771395fb-775d-462e-86dc-0600cfecb345
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 5%

---

# CarouselView.frametransition{#carouselview-frametransition}

` [CarouselView.|<containerId>_carouselView.]frametransition=none|fade|slide[, *``*[, *`持續間距`*]`

<table id="table_D5992FCFF26046079089652B211BB6C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 無|淡化|幻燈片  </span> </p> </td> 
   <td colname="col2"> <p>指定對幀更改應用的效果類型。 <span class="codeph"> 無 </span> 代表無轉變；框架變化會立即發生。 </p> <p> <span class="codeph"> 淡 </span> 出表示新舊幀之間的交叉淡出過渡。 </p> <p> <span class="codeph"> 滑 </span> 塊激活過渡，舊框架滑出視圖，新框架滑入。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 持續時間  </span> </span> </p> </td> 
   <td colname="col2"> <p>指定<span class="codeph">淡化</span>或<span class="codeph">幻燈片</span>過渡效果的持續時間（秒）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 間距  </span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">滑動</span>過渡中相鄰幀之間的間隔，其範圍在<span class="codeph"> 0 </span>和<span class="codeph"> 1 </span>之間，並且是相對於元件的寬度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

選填。

## 預設 {#section-71fb773f814649b2885aefee68073641}

無。

## 範例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`frametransition=fade,0.3`
