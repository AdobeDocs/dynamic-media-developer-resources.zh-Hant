---
description: FlyoutZoomView.fmt
solution: Experience Manager
title: FlyoutZoomView.fmt
feature: Dynamic Media Classic，檢視器，SDK/API,Flyout
role: Developer,Business Practitioner
exl-id: 4e1ce754-6967-492b-a617-764ee3ec3a55
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 4%

---

# FlyoutZoomView.fmt{#flyoutzoomview-fmt}

`[FlyoutZoomView.|<containerId>_flyout.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_12B0B59D83BC40FCB957F41B331A1EF9"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif|alpha</span> </p> </td> 
   <td colname="col2"> <p> 指定元件用於從影像伺服器載入影像的影像格式。 如果指定的格式結尾為<span class="codeph"> "-alpha"</span>，則元件會將影像呈現為透明內容。 對於所有其他影像格式，元件將影像視為不透明。 請注意，元件預設為白色背景。 因此，若要使其完全透明，請將<span class="codeph"> background-color</span> CSS屬性設為<span class="codeph"> transparent</span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

選填。

## 預設 {#section-a08032f0fcf041c09e63c0238a339fc9}

`jpeg`

## 範例 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`fmt=png-alpha`
