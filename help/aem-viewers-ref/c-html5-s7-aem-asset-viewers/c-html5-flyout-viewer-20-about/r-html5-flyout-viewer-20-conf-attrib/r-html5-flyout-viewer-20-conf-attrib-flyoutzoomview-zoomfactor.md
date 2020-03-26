---
description: 'null'
seo-description: 'null'
seo-title: FlyoutZoomView.zoomfactor
solution: Experience Manager
title: FlyoutZoomView.zoomfactor
topic: Dynamic media
uuid: 58d49de7-4828-46ae-b2e7-eb9398e98a99
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# FlyoutZoomView.zoomfactor{#flyoutzoomview-zoomfactor}

` [FlyoutZoomView.|<containerId>_flyout.]zoomfactor= *`primaryFactorysecondaryFactorusplay`*[,[ *``*][, *``*]]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> primaryFactor</span></span> </p> </td> 
   <td colname="col2"> <p> 指定相對於主視圖的彈出視圖的影像放大率。必須是整數或浮點值 <span class="codeph"> 1.0</span> 或更大。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> secondaryFactor <span class="varname"></span></span> </p> </td> 
   <td colname="col2"> <p> 可以指定可選次要因素，當反白顯示處於活動狀態時，按一下或點選主視圖即可訪問該次要因素。 按一下或點選第二次會回復為主要縮放比例。 值-1會 <span class="codeph"> 停用次要縮放系數</span> 。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 高檔</span></span> </p> </td> 
   <td colname="col2"> <p>指定元件處理小影像的方式。 </p> <p>如果設為 <span class="codeph"> 1</span> ，元件會放大主影像，使其適合主檢視。 此外，它還會縮放縮放縮放影像，使其完全填滿已設定的彈出視窗區域。 </p> <p>如果設為 <span class="codeph"> 0</span> ，則會以原始解析度顯示小影像，並在主檢視區域和彈出視窗中置中顯示。 您可以在主檢視和彈出視窗中，分別使用 <span class="codeph"> s7flyoutzoomview</span> 和 <span class="codeph"> s7flyoutzoom</span> CSS類別的背景或類似CSS屬性，設定出現在影像周圍的額外空格。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

選填。

## 預設 {#section-a08032f0fcf041c09e63c0238a339fc9}

`3,-1,1`

## 範例 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`zoomfactor=2,3,0`
