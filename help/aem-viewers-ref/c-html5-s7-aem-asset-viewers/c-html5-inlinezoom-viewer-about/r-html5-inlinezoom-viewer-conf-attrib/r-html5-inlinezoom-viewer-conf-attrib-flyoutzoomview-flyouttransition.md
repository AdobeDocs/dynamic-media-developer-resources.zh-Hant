---
description: 'null'
seo-description: 'null'
seo-title: FlyoutZoomView.flyouttransition
solution: Experience Manager
title: FlyoutZoomView.flyouttransition
topic: Dynamic media
uuid: 0b94956d-9ee6-409e-9b52-29c888932a0e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# FlyoutZoomView.flyouttransition{#flyoutzoomview-flyouttransition}

` [FlyoutZoomView.|<containerId>_flyout.]flyouttransition=[none|slide|fade][, *``*[, *``*[, *``*[, *`showtimeshowdelayhidetimehidedelay`*]]]]`

<table id="table_AB421835D2454ECD8AA40DBFADBAC65F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 無|slide|fade </span></span> </p> </td> 
   <td colname="col2"> <p> 指定顯示或隱藏彈出視圖時應用的效果的類型。 如果沒 <span class="codeph"> 有， </span>則會在啟動並準備好時立即顯示彈出影像；投 <span class="codeph"> 影片 </span> 可讓投影片動畫以左右方向播放；淡 <span class="codeph"> 出 </span> 會將alpha轉場套用至彈出式影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> showtime </span></span> </p> </td> 
   <td colname="col2"> <p> 顯示動畫完成的秒數。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> showdelay </span></span> </p> </td> 
   <td colname="col2"> <p> 啟動顯示動畫的使用者動作與顯示動畫本身開始之間的秒數延遲。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 隱藏時 </span> 間 </span> </p> </td> 
   <td colname="col2"> <p> 隱藏動畫完成所需的秒數。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 隱藏延遲 </span> </span> </p> </td> 
   <td colname="col2"> <p> 啟動隱藏動畫的使用者動作與隱藏動畫本身開始之間的秒數延遲。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-e6310c8c4e8547689a5b48ceddb3671d}

選填。

## 預設 {#section-fcb06fd8e7e945e590094efcf9a1d510}

`fade,1,0,1,0`

## 範例 {#section-3a188ab955c445bcb2efa3c49722c10d}

`flyouttransition=slide,1,1,2,1`
