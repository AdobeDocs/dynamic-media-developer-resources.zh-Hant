---
description: 'null'
seo-description: 'null'
seo-title: ZoomView.enableHD
solution: Experience Manager
title: ZoomView.enableHD
topic: Dynamic media
uuid: 5badee0b-3bbc-4306-bc60-a606775db2bd
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 7%

---


# ZoomView.enableHD{#zoomview-enablehd}

` [ZoomView.|<containerId>_zoomView.]enableHD=always|never|limit[, *`數字`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> always|never|limit</span> </p> </td> 
   <td colname="col2"> <p> 對<span class="codeph"> devicePixelRatio</span>大於<span class="codeph"> 1</span>的裝置啟用、限制或停用最佳化。 影響具有高密度顯示的裝置，例如iPhone4和類似裝置。 如果活動，該元件將限制IS影像請求的大小，好像該設備具有<span class="codeph"> 1</span>的像素比，從而減少頻寬。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 數字</span></span> </p> </td> 
   <td colname="col2"> <p> 如果使用限制設定，元件僅會啟用高像素密度，而達到指定的限制。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

選填。

## 預設 {#section-71fb773f814649b2885aefee68073641}

`limit,1500`

## 範例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`enableHD=always`
