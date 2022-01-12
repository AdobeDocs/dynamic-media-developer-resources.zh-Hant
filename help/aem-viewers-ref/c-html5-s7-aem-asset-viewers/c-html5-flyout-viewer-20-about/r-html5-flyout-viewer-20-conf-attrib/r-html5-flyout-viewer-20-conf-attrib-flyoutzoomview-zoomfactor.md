---
title: FlyoutZoomView.zoomfactor
description: FlyoutZoomView.zoomfactor
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 150968d2-aece-4d2a-b5a8-31b03dae25bb
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 2%

---

# FlyoutZoomView.zoomfactor{#flyoutzoomview-zoomfactor}

` [FlyoutZoomView.|<containerId>_flyout.]zoomfactor= *`primaryFactor`*[,[ *`secondaryFactor`*][, *`高檔`*]]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> primaryFactor</span> </span> </p> </td> 
   <td colname="col2"> <p> 指定彈出視圖的影像放大率（相對於主視圖）。必須是整數或浮點值 <span class="codeph"> 1.0</span> 或更大。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> secondaryFactor</span> </span> </p> </td> 
   <td colname="col2"> <p> 可以指定可選次要因素，當突出顯示活動時，按一下或點選主視圖即可訪問該次要因素。 按一下或點選第二次會回復成主要縮放因子。 值 <span class="codeph"> -1</span> 禁用次縮放因子。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 高檔</span></span> </p> </td> 
   <td colname="col2"> <p>指定元件處理小影像的方式。 </p> <p>若設為 <span class="codeph"> 1</span> 元件會上調主影像，使其適合主檢視。 此外，它會上調縮放影像，以便完全填滿已設定的彈出窗口區域。 </p> <p>若設為 <span class="codeph"> 0</span>，小影像以其原始解析度顯示，並在主視區和彈出窗口內置中顯示。 您可以使用的背景或類似的CSS屬性，設定出現在影像周圍的額外空白字元 <span class="codeph"> s7flyoutzoomview</span> 和 <span class="codeph"> s7flyoutzoom</span> 主要檢視和彈出視窗中的CSS類別。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

選填。

## 預設 {#section-a08032f0fcf041c09e63c0238a339fc9}

`3,-1,1`

## 範例 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`zoomfactor=2,3,0`
