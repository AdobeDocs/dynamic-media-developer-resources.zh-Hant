---
title: ZoomView.enableHD
description: ZoomView.enableHD
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: b3cc32ef-dd6c-47a3-9e55-86a43e874a84
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# ZoomView.enableHD{#zoomview-enablehd}

` [ZoomView.|<containerId>_zoomView.]enableHD=always|never|limit[, *`數字`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 一律|從不|限制</span> </p> </td> 
   <td colname="col2"> <p> 啟用、限制或停用<span class="codeph"> devicePixelRatio</span>大於<span class="codeph"> 1</span>的裝置最佳化。 影響具有高密度顯示的裝置，如iPhone4和類似裝置。 如果活動，則元件將限制IS影像請求的大小，就像設備的像素比<span class="codeph"> 1</span>一樣，從而減少頻寬。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 數字</span></span> </p> </td> 
   <td colname="col2"> <p> 如果使用限制設定，元件僅會啟用高像素密度，而最高可達指定的限制。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

選填。

## 預設 {#section-71fb773f814649b2885aefee68073641}

`limit,1500`

## 範例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`enableHD=always`
