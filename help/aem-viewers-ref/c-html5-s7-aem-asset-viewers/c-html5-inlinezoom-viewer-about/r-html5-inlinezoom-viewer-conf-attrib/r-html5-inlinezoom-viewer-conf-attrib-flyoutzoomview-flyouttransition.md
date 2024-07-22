---
title: FlyoutZoomView.flyouttransition
description: FlyoutZoomView.flyouttransition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 3199d4a3-4799-40a2-b0a5-0e1ee4744fbe
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '119'
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

## 屬性 {#section-e6310c8c4e8547689a5b48ceddb3671d}

選擇性.

## 預設 {#section-fcb06fd8e7e945e590094efcf9a1d510}

`fade,1,0,1,0`

## 範例 {#section-3a188ab955c445bcb2efa3c49722c10d}

`flyouttransition=slide,1,1,2,1`
