---
description: FlyoutZoomView.preloadtiles
solution: Experience Manager
title: FlyoutZoomView.preloadtiles
feature: Dynamic Media Classic，檢視器，SDK/API，內嵌縮放
role: Developer,User
exl-id: f50ea45a-afd5-4e4f-967d-c45cecc5fb7b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '68'
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

## 屬性 {#section-e6310c8c4e8547689a5b48ceddb3671d}

選填。

## 預設 {#section-fcb06fd8e7e945e590094efcf9a1d510}

`0`

## 範例 {#section-3a188ab955c445bcb2efa3c49722c10d}

`preloadtiles=1`
