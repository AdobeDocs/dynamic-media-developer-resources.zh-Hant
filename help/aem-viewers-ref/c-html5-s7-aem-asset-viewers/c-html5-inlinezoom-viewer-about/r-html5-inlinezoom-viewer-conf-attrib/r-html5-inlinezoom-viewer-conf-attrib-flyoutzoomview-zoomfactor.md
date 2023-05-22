---
title: FlyoutZoomView.zoomfactor
description: FlyoutZoomView.zoomfactor
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 2a9d4450-a1a0-471c-86bf-105d516b0bd7
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 1%

---

# FlyoutZoomView.zoomfactor{#flyoutzoomview-zoomfactor}

` [FlyoutZoomView.|<containerId>_flyout.]zoomfactor= *`primaryFactor`*[,[ *`次因子`*][, *`高檔`*]]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> primaryFactor</span> </span> </p> </td> 
   <td colname="col2"> <p> 指定相對於主視圖的浮出視圖的影像放大率。 必須是整數或浮點值 <span class="codeph"> 1.0</span> 或更大。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 次因子</span> </span> </p> </td> 
   <td colname="col2"> <p> 可指定可選的輔助因子，當高亮顯示處於活動狀態時，按一下或輕擊主視圖即可訪問輔助因子。 按一下或點擊第二次將恢復為主縮放因子。 值 <span class="codeph"> -1</span> 禁用輔助縮放因子。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 高檔</span></span> </p> </td> 
   <td colname="col2"> <p>指定元件處理小影像的方式。 </p> <p>如果設定為 <span class="codeph"> 1</span> 該元件對主影像進行上縮放，使其適合主視圖。 此外，它會升級縮放影像，以便它完全填充配置的彈出窗口區域。 </p> <p>如果設定為 <span class="codeph"> 0</span>，以其原始解析度顯示小影像，並在主視區和彈出窗口的中心顯示。 可以使用的背景或類似CSS屬性配置影像周圍的額外空白 <span class="codeph"> S7蠅</span> 和 <span class="codeph"> s7蠅縮放</span> 主視圖和彈出窗口中的CSS類。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-e6310c8c4e8547689a5b48ceddb3671d}

選擇性.

## 預設 {#section-fcb06fd8e7e945e590094efcf9a1d510}

`3,-1,1`

## 範例 {#section-3a188ab955c445bcb2efa3c49722c10d}

`zoomfactor=2,3,0`
