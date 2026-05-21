---
title: FlyoutZoomView.imagereload
description: FlyoutZoomView.imagereload
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 483fa64b-5196-4477-8ea6-0f32c6557f72
TQID: 'https://experienceleague.adobe.com/nkYQwtTb1AUBLBbnN2HwMZLIjyolj5l-6CxEy-yEo3k'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 120
ht-degree: 4%

---

# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *`寬度`*[; *`寬度`*]]`

<table id="table_42CA0074AD7C4F0D9FC81E9FCB0591C0"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> 設定在調整大小期間，元件如何擷取主檢視和彈出式檢視的新影像。 </p> <p>設定為<span class="codeph"> 0 </span>時，在調整大小期間元件不會載入新影像；彈出式檢視中的影像解析度不會變更。 </p> <p>設定為<span class="codeph"> 1 </span>可讓您為載入至主檢視的影像指定一或多個寬度中斷點。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">中斷點，<span class="varname">寬度</span>[； <span class="varname">寬度</span>] </span> </p> </td> 
   <td colname="col2"> <p> 載入主檢視的影像寬度中斷點。 元件始終使用最佳配合大小來初始載入。 在調整大小後，這可確保下載主檢視中的影像時，寬度一律等於最接近的大型中斷點，並在使用者端上縮小比例。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

選擇性.

## 預設 {#section-a08032f0fcf041c09e63c0238a339fc9}

`0`

## 範例 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`imagereload=1,breakpoint,200;400;800;1600`
