---
title: ZoomView.singleclick
description: ZoomView.singleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 3fd5b907-faf6-4d36-8ee1-79f3ace781d4
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 3%

---

# ZoomView.singleclick{#zoomview-singleclick}

`[ZoomView.|<containerId>_zoomView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 無|縮放|重置|縮放重置 </span> </p> </td> 
   <td colname="col2"> <p> 配置按一下/點擊的映射以縮放操作。 設定為 <span class="codeph"> 無 </span> 禁用按一下/點擊縮放。 如果設定為 <span class="codeph"> 縮放 </span> 按一下影像可縮放一個縮放步驟；CTRL+按一下可縮小一個縮放步驟。 設定為 <span class="codeph"> 重置 </span> 使按一下影像將縮放重置為初始縮放級別。 對於 <span class="codeph"> 縮放重置 </span>，如果當前縮放因子達到或超過指定限制，則應用重置，否則應用縮放。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

選擇性.

## 預設 {#section-71fb773f814649b2885aefee68073641}

`zoomReset`  — 在台式電腦上； `none` 觸摸設備。

## 範例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`singleclick=zoom`
