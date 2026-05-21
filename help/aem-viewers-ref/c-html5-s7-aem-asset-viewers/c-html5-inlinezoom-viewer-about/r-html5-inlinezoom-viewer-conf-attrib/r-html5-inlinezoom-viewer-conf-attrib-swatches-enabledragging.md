---
title: 色票.enabledragging
description: 色票.enabledragging
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 9b69f6d7-b7a1-42c6-98d7-80952b7f8b31
TQID: 'https://experienceleague.adobe.com/HHYegiojXgmu3TnynjtLNjV6lhWuKkJT1-8QN1Mp2F8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 80
ht-degree: 6%

---

# 色票.enabledragging{#swatches-enabledragging}

` [Swatches.|<containerId>_swatches.]enabledragging=0|1[, *`overdragvalue`*]`

<table id="table_B1363BFD20204093AAB326A1AB503B93"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td> <p> 啟用或停用使用者利用滑鼠或觸控手勢捲動色票的能力 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> <span class="varname"> overdragvalue </span> </span> </p> </td> 
   <td> <p> 在<span class="codeph"> 0-1 </span>範圍內的函式。 這是以實際速度在錯誤方向移動的<span class="codeph"> % </span>值。 如果設定為<span class="codeph"> 1 </span>，它會隨滑鼠移動。 如果設定為<span class="codeph"> 0 </span>，則完全不允許您向錯誤的方向移動。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-e6310c8c4e8547689a5b48ceddb3671d}

選擇性.

## 預設 {#section-fcb06fd8e7e945e590094efcf9a1d510}

`1,0.5`

## 範例 {#section-3a188ab955c445bcb2efa3c49722c10d}

`enabledragging=0`
