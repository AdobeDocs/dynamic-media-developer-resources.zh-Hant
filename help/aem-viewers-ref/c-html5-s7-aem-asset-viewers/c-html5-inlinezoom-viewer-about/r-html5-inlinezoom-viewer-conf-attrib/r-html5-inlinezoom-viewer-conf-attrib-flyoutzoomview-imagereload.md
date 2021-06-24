---
description: FlyoutZoomView.imagereload
solution: Experience Manager
title: FlyoutZoomView.imagereload
feature: Dynamic Media Classic，檢視器，SDK/API，內嵌縮放
role: Developer,Business Practitioner
exl-id: 84dd1e40-2ab8-4356-9eff-8766432b539b
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 3%

---

# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *``*[; *`widthwidth`*]]`

<table id="table_7DA232CB62134078B788B9AB1452F363"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> 配置元件在調整大小期間如何為主視圖和彈出視圖獲取新映像。 </p> <p>設為<span class="codeph"> 0 </span>時，元件在調整大小期間不會載入新影像，且彈出檢視中的影像解析度不會變更。 </p> <p>設為<span class="codeph"> 1 </span>可讓您為載入到主檢視的影像指定一個或多個寬度斷點。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 斷點， <span class="varname"> 寬度 </span>; <span class="varname"> 寬度  </span> </span> </p> </td> 
   <td colname="col2"> <p>載入到主視圖的影像的寬度斷點。 </p> <p>元件在初始載入時始終使用最合適的大小。 調整大小後，它可確保始終使用等於最接近的較大斷點的寬度下載主視圖中的影像，並在客戶端上縮小。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-e6310c8c4e8547689a5b48ceddb3671d}

選填。

## 預設 {#section-fcb06fd8e7e945e590094efcf9a1d510}

`1,breakpoint,300;600;1200`

## 範例 {#section-3a188ab955c445bcb2efa3c49722c10d}

`imagereload=1,breakpoint,200;400;800;1600`
