---
description: FlyoutZoomView.imagereload
solution: Experience Manager
title: FlyoutZoomView.imagereload
feature: Dynamic Media Classic，檢視器，SDK/API,Flyout
role: Developer,Business Practitioner
exl-id: 483fa64b-5196-4477-8ea6-0f32c6557f72
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 4%

---

# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *``*[; *`widthwidth`*]]`

<table id="table_42CA0074AD7C4F0D9FC81E9FCB0591C0"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> 配置元件在調整大小期間如何為主視圖和彈出視圖獲取新映像。 </p> <p>設為<span class="codeph"> 0 </span>時，元件在調整大小期間不會載入新影像；飛出檢視中的影像解析度不會變更。 </p> <p>設定為<span class="codeph"> 1 </span>可讓您為載入到主檢視的影像指定一個或多個寬度斷點。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 斷點， <span class="varname"> 寬度 </span>[; <span class="varname"> width  </span>]  </span> </p> </td> 
   <td colname="col2"> <p> 載入到主視圖的影像的寬度斷點。 元件在初始載入時始終使用最合適的大小。 調整大小後，它可確保始終下載主視圖中的影像，其寬度等於最接近的大斷點，並在客戶端上縮放。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

選填。

## 預設 {#section-a08032f0fcf041c09e63c0238a339fc9}

`0`

## 範例 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`imagereload=1,breakpoint,200;400;800;1600`
