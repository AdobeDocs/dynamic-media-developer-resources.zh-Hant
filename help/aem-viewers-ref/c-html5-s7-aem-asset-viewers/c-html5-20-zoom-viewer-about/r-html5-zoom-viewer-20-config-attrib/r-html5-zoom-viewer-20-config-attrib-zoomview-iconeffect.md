---
title: ZoomView.iconeffect
description: ZoomView.iconeffect
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 59d71d3b-706f-4f77-8e75-e24c5654f6e3
TQID: 'https://experienceleague.adobe.com/kkASM0uYyw3UqHWf-AVpztZvnpWg4t7djmqVkFWAxR4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: f6432244ef9faba7a81488e9de8e438154ae6123
workflow-type: tm+mt
source-wordcount: 120
ht-degree: 4%

---

# ZoomView.iconeffect{#zoomview-iconeffect}

` [ZoomView.|<containerId>_zoomView.]iconeffect=0|1[, *`計數`*][, *`淡化`*][, *`自動隱藏`*]`

<table id="table_6CAA904E976A41BD994D8926F46F0BAF"> 
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

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

選擇性.

## 預設 {#section-71fb773f814649b2885aefee68073641}

`1,1,0.3,3`

## 範例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`iconeffect=0`

