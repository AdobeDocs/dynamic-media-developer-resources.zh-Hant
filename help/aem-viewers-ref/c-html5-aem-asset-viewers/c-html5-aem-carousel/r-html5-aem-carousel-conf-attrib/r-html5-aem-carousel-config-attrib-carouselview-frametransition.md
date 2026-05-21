---
title: CarouselView.frametransition
description: CarouselView.frametransition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 771395fb-775d-462e-86dc-0600cfecb345
TQID: 'https://experienceleague.adobe.com/65cLC5DOqdGrbVpMMy6gLBNL4F3WRqipNqIlpBIK-GM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 97
ht-degree: 4%

---

# CarouselView.frametransition{#carouselview-frametransition}

` [CarouselView.|<containerId>_carouselView.]frametransition=none|fade|slide[, *`持續時間`*[, *`間距`*]`

<table id="table_D5992FCFF26046079089652B211BB6C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">無|淡化|投影片</span> </p> </td> 
   <td colname="col2"> <p>指定套用到影格變更的效果型別。 例如，<span class="codeph"> none </span>表示無轉變；畫面格變更會立即發生。 和 </p> <p> <span class="codeph">淡化</span>表示舊影格和新影格之間的交叉淡入淡出切換。 最後， </p> <p> <span class="codeph">張投影片</span>會啟動轉變，舊框架會滑出檢視，新框架會滑入。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">期間</span> </span> </p> </td> 
   <td colname="col2"> <p>指定<span class="codeph">淡化</span>或<span class="codeph">幻燈片</span>切換效果的持續時間（以秒為單位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">間距</span> </span> </p> </td> 
   <td colname="col2"> <p>在<span class="codeph">投影片</span>轉換中相鄰影格之間的間距，範圍介於<span class="codeph"> 0 </span>到<span class="codeph"> 1 </span>之間，且與元件的寬度相關。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

選擇性.

## 預設 {#section-71fb773f814649b2885aefee68073641}

無。

## 範例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`frametransition=fade,0.3`
