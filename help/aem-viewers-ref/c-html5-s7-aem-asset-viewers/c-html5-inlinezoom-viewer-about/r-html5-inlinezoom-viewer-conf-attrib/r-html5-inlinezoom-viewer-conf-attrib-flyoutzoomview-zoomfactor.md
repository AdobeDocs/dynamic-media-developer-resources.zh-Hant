---
description: FlyoutZoomView.zoomfactor
solution: Experience Manager
title: FlyoutZoomView.zoomfactor
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 2%

---


# FlyoutZoomView.zoomfactor{#flyoutzoomview-zoomfactor}

` [FlyoutZoomView.|<containerId>_flyout.]zoomfactor= *`primaryFactorysecondaryFactorusplay`*[,[ *``*][, *``*]]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> primaryFactor</span> </span> </p> </td> 
   <td colname="col2"> <p> 指定相對於主視圖的彈出視圖的影像放大率。必須是整數或浮點值<span class="codeph"> 1.0</span>或更大。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> secondaryFactor</span> </span> </p> </td> 
   <td colname="col2"> <p> 可以指定可選次要因素，當反白顯示處於活動狀態時，按一下或點選主視圖即可訪問該次要因素。 按一下或點選第二次會回復為主要縮放比例。 值<span class="codeph"> -1</span>會停用次要縮放系數。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 高檔</span></span> </p> </td> 
   <td colname="col2"> <p>指定元件處理小影像的方式。 </p> <p>如果設為<span class="codeph"> 1</span>，元件會放大主影像，使其適合主檢視。 此外，它還會縮放縮放縮放影像，使其完全填滿已設定的彈出視窗區域。 </p> <p>如果設定為<span class="codeph"> 0</span>，則以其原始解析度顯示小影像，並在主視圖區域和彈出窗口中居中顯示。 您可以在主檢視和彈出視窗中，分別使用<span class="codeph"> s7flyoutzoomview</span>和<span class="codeph"> s7flyoutzoom</span> CSS類別的背景或類似CSS屬性，來設定影像周圍的額外空白。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-e6310c8c4e8547689a5b48ceddb3671d}

選填。

## 預設 {#section-fcb06fd8e7e945e590094efcf9a1d510}

`3,-1,1`

## 範例 {#section-3a188ab955c445bcb2efa3c49722c10d}

`zoomfactor=2,3,0`
