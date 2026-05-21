---
title: FlyoutZoomView.zoomfactor
description: FlyoutZoomView.zoomfactor
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 150968d2-aece-4d2a-b5a8-31b03dae25bb
TQID: 'https://experienceleague.adobe.com/Zp4VYoGBfivwXRZQ7dmtouoy2qFMZePQKDrocHaBPXk'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 178
ht-degree: 1%

---

# FlyoutZoomView.zoomfactor{#flyoutzoomview-zoomfactor}

` [FlyoutZoomView.|<containerId>_flyout.]zoomfactor= *`primaryFactor`*[,[ *`secondaryFactor`*][, *`升級`*]]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> primaryFactor</span> </span> </p> </td> 
   <td colname="col2"> <p> 指定彈出檢視相對於主檢視的影像放大比例。 必須是整數或浮點值<span class="codeph"> 1.0</span>或更大。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> secondaryFactor</span> </span> </p> </td> 
   <td colname="col2"> <p> 當反白顯示處於作用中狀態時，按一下或點選主檢視可存取的選擇性次要因數。 按一下或點選第二次會回覆為主要縮放因數。 值為<span class="codeph"> -1</span>會停用次要縮放因數。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname">升級</span></span> </p> </td> 
   <td colname="col2"> <p>指定元件處理小型影像的方式。 </p> <p>若設為<span class="codeph"> 1</span>，元件會放大主影像，使其符合主檢視。 此外，它也會放大縮放影像，以完全填滿已設定的彈出式視窗區域。 </p> <p>若設為<span class="codeph"> 0</span>，小型影像會以其原始解析度顯示，並置中顯示在主檢視區域和彈出式視窗內。 您可以分別在主檢視和彈出式視窗中，以<span class="codeph"> s7flyoutzoomview</span>和<span class="codeph"> s7flyoutzoom</span> CSS類別的背景或類似CSS屬性，設定影像周圍出現的額外空格。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

選擇性.

## 預設 {#section-a08032f0fcf041c09e63c0238a339fc9}

`3,-1,1`

## 範例 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`zoomfactor=2,3,0`
