---
title: FlyoutZoomView.flyouttransition
description: FlyoutZoomView.flyouttransition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: a15723fe-a8be-49c5-bad3-1a1360eeb232
TQID: 'https://experienceleague.adobe.com/iruR3DHgjvkhRkUii2qvRjpbFSxRHsbT4hKfwSMqXtg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 118
ht-degree: 2%

---

# FlyoutZoomView.flyouttransition{#flyoutzoomview-flyouttransition}

` [FlyoutZoomView.|<containerId>_flyout.]flyouttransition=[none|slide|fade][, *`顯示時間`*[, *`顯示延遲`*[, *`隱藏時間`*[, *`隱藏延遲`*]]]]`

<table id="table_AB421835D2454ECD8AA40DBFADBAC65F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> none|slide|fade </span> </span> </p> </td> 
   <td colname="col2"> <p> 指定顯示或隱藏彈出式檢視時套用的效果型別。 使用<span class="codeph">無</span>，彈出式影像會在啟動並準備就緒時立即顯示；<span class="codeph">投影片</span>會以由左至右的方向播放投影片動畫；<span class="codeph">淡化</span>會套用Alpha轉換至彈出式影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">顯示時間</span> </span> </p> </td> 
   <td colname="col2"> <p> 完成顯示動畫所需的秒數。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">顯示延遲</span> </span> </p> </td> 
   <td colname="col2"> <p> 啟動顯示動畫的使用者動作與顯示動畫本身開始之間的延遲秒數。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">隱藏時間</span> </span> </p> </td> 
   <td colname="col2"> <p> 隱藏動畫完成所需的秒數。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">隱藏延遲</span> </span> </p> </td> 
   <td colname="col2"> <p> 啟動隱藏動畫的使用者動作與隱藏動畫本身開始之間的延遲秒數。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

選擇性.

## 預設 {#section-a08032f0fcf041c09e63c0238a339fc9}

`fade,1,0,1,0`

## 範例 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`flyouttransition=slide,1,1,2,1`
