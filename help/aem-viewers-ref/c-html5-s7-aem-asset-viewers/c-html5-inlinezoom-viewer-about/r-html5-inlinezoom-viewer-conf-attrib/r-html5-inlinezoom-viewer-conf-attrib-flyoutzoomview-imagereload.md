---
description: FlyoutZoomView.imagereload
solution: Experience Manager
title: FlyoutZoomView.imagereload
feature: Dynamic Media經典，檢視器，SDK/API，內嵌縮放
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 3%

---


# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *`寬`*[; *`度`*]]`

<table id="table_7DA232CB62134078B788B9AB1452F363"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> 配置元件在調整大小期間如何為主視圖和彈出視圖讀取新影像。 </p> <p>設為<span class="codeph"> 0 </span>時，元件在調整大小時不會載入新影像，而彈出檢視中的影像解析度也不會變更。 </p> <p>設為<span class="codeph"> 1 </span>可讓您為載入主檢視的影像指定一或多個寬度中斷點。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 斷點、 <span class="varname"> 寬度 </span>; <span class="varname"> 寬度  </span> </span> </p> </td> 
   <td colname="col2"> <p>載入主檢視之影像的寬度中斷點。 </p> <p>元件在初始載入時始終使用最佳尺寸。 調整大小後，它可確保使用等於最接近較大斷點的寬度來下載主檢視中的影像，並在用戶端上縮放。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-e6310c8c4e8547689a5b48ceddb3671d}

選填。

## 預設 {#section-fcb06fd8e7e945e590094efcf9a1d510}

`1,breakpoint,300;600;1200`

## 範例 {#section-3a188ab955c445bcb2efa3c49722c10d}

`imagereload=1,breakpoint,200;400;800;1600`
