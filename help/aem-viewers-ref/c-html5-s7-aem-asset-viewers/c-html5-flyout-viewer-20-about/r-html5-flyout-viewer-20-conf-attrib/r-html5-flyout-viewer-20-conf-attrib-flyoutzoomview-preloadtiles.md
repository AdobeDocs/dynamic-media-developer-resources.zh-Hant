---
description: FlyoutZoomView.preloadtiles
solution: Experience Manager
title: FlyoutZoomView.preloadtiles
feature: Dynamic Media Classic，檢視器，SDK/API,Flyout
role: Developer,Business Practitioner
exl-id: 34c8c7b9-0369-4d13-95f5-ad129e913453
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 7%

---

# FlyoutZoomView.preloadtiles{#flyoutzoomview-preloadtiles}

`[FlyoutZoomView.|<containerId>_flyout.]preloadtiles=0|1`

<table id="table_8E44EC404A1A45C59EA1EF2766613930"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> 設為<span class="codeph"> 1</span>以啟用預先載入縮放影像，或設為<span class="codeph"> 0</span>以視需要遞增載入縮放影像。 </p> <p> <p>注意： 如果啟用此選項，可能會導致頻寬使用率顯著提高。 縮放影像會完整載入，即使使用者未起始縮放動作亦然。 </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

選填。

## 預設 {#section-a08032f0fcf041c09e63c0238a339fc9}

`0`

## 範例 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`preloadtiles=1`
