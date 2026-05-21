---
title: FlyoutZoomView.preloadtiles
description: FlyoutZoomView.preloadtiles
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 34c8c7b9-0369-4d13-95f5-ad129e913453
TQID: 'https://experienceleague.adobe.com/z4hvMPsPhAjJM1n0Oxz9GpIXFEXSFg-HynKye4CkN-I'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 63
ht-degree: 7%

---

# FlyoutZoomView.preloadtiles{#flyoutzoomview-preloadtiles}

`[FlyoutZoomView.|<containerId>_flyout.]preloadtiles=0|1`

<table id="table_8E44EC404A1A45C59EA1EF2766613930"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> 設為<span class="codeph"> 1</span>以啟用預先載入縮放影像，或設為<span class="codeph"> 0</span>以視需要增量載入縮放影像。 </p> <p> <p>注意：如果啟用此選項，可能會大幅增加頻寬使用量。 縮放的影像會完整載入，即使使用者未起始縮放動作亦然。 </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

選擇性.

## 預設 {#section-a08032f0fcf041c09e63c0238a339fc9}

`0`

## 範例 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`preloadtiles=1`
