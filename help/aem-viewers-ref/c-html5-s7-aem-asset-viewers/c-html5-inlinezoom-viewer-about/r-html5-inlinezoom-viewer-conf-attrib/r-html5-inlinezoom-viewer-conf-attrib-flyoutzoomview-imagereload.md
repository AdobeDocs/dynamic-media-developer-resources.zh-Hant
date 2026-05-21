---
title: FlyoutZoomView.imagereload
description: FlyoutZoomView.imagereload
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 84dd1e40-2ab8-4356-9eff-8766432b539b
TQID: 'https://experienceleague.adobe.com/utzPqD5UMx7TnJK8FvqflzoSjOWGVaGXhKlviY1U9xQ'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 123
ht-degree: 4%

---

# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *`寬度`*[; *`寬度`*]]`

<table id="table_7DA232CB62134078B788B9AB1452F363"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> 設定在調整大小期間，元件如何擷取主檢視和彈出式檢視的新影像。 </p> <p>設定為<span class="codeph"> 0 </span>，調整大小期間元件未載入新影像，而且彈出式檢視中的影像解析度不會變更。 </p> <p>設定為<span class="codeph"> 1 </span>可讓您為載入至主檢視的影像指定一或多個寬度中斷點。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">中斷點，<span class="varname">寬度</span>；<span class="varname">寬度</span> </span> </p> </td> 
   <td colname="col2"> <p>載入主檢視的影像寬度中斷點。 </p> <p>元件始終使用最佳配合大小來初始載入。 在調整大小之後，它可確保主檢視中的影像一律使用等於最接近較大中斷點的寬度下載，並在使用者端上縮小比例。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-e6310c8c4e8547689a5b48ceddb3671d}

選擇性.

## 預設 {#section-fcb06fd8e7e945e590094efcf9a1d510}

`1,breakpoint,300;600;1200`

## 範例 {#section-3a188ab955c445bcb2efa3c49722c10d}

`imagereload=1,breakpoint,200;400;800;1600`
