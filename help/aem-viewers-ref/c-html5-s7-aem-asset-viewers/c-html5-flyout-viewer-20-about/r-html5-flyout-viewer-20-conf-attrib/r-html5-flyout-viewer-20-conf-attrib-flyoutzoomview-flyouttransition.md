---
title: FlyoutZoomView.flyouttransition
description: FlyoutZoomView.flyouttransition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: a15723fe-a8be-49c5-bad3-1a1360eeb232
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 2%

---

# FlyoutZoomView.flyouttransition{#flyoutzoomview-flyouttransition}

` [FlyoutZoomView.|<containerId>_flyout.]flyouttransition=[none|slide|fade][, *`顯示時間`*[, *`延遲`*[, *`隱蔽時間`*[, *`隱藏`*]]]]`

<table id="table_AB421835D2454ECD8AA40DBFADBAC65F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 無|幻燈片|淡入 </span> </span> </p> </td> 
   <td colname="col2"> <p> 指定顯示或隱藏浮出視圖時應用的效果的類型。 與 <span class="codeph"> 無 </span>激活後立即出現； <span class="codeph"> 滑 </span> 使幻燈片動畫從左向右播放； <span class="codeph"> 淡 </span> 將Alpha過渡應用於浮出影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 顯示時間 </span> </span> </p> </td> 
   <td colname="col2"> <p> 演示動畫完成的秒數。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 延遲 </span> </span> </p> </td> 
   <td colname="col2"> <p> 啟動顯示動畫的用戶操作與顯示動畫本身的開始之間的延遲（秒）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 隱蔽時間 </span> </span> </p> </td> 
   <td colname="col2"> <p> 隱藏動畫完成所需的秒數。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 隱藏 </span> </span> </p> </td> 
   <td colname="col2"> <p> 啟動隱藏動畫的用戶操作與隱藏動畫本身的開始之間的延遲（秒）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

選擇性.

## 預設 {#section-a08032f0fcf041c09e63c0238a339fc9}

`fade,1,0,1,0`

## 範例 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`flyouttransition=slide,1,1,2,1`
