---
title: PageView.iconEffect
description: PageView.iconEffect
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: cdd96e58-d805-47d6-bf26-9ebd90afd535
TQID: 'https://experienceleague.adobe.com/BChSE62IgfhsabTf1I-XlAJLqvRhai4U48vNEg-MkQ4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 120
ht-degree: 4%

---

# PageView.iconEffect{#pageview-iconeffect}

` [PageView.|<containerId>_pageView.]iconeffect=0|1[, *`計數`*][, *`淡化`*][, *`自動隱藏`*]`

<table id="table_DD66FFC263A34220876DD204BFE62D49"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> 啟用<span class="codeph"> iconeffect</span>，以便在影像處於重設狀態時顯示在影像上方，並暗示有可與影像互動的動作。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname">計數</span></span> </p> </td> 
   <td colname="col2"> <p> 指定<span class="codeph"> iconeffect</span>出現和重新出現的最大次數。 值為<span class="codeph"> -1</span>表示圖示永遠無限期地重新出現。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname">淡化</span></span> </p> </td> 
   <td colname="col2"> <p>指定顯示或隱藏動畫的持續時間（秒）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname">自動隱藏</span></span> </p> </td> 
   <td colname="col2"> <p>設定<span class="codeph"> iconeffect</span>在自動隱藏之前保持完全可見的秒數。 亦即，淡入動畫完成之後、淡出動畫開始之前的時間。 設定為<span class="codeph"> 0</span>會停用自動隱藏行為。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-b6e5e52698d4492f9d6350e7e312bb1b}

選擇性.

## 預設 {#section-7d0fc8fa09b34c288ed32ef7faa84604}

`1,1,0.3,3`

## 範例 {#section-95db1bfcccf241089654363203b19977}

`iconeffect=0`
