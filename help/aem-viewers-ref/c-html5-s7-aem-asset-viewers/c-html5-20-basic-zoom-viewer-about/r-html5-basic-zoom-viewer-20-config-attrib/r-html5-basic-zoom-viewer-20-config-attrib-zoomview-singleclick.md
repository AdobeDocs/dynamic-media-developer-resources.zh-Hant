---
title: ZoomView.singleclick
description: ZoomView.singleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: c2292b5b-5b4e-4368-9495-9108042ec2f1
source-git-commit: 7eddc50fb9803eacdd1f513c6132380793b6f88d
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 4%

---

# ZoomView.singleclick{#zoomview-singleclick}

`[ZoomView.|<containerId>_zoomView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 無|縮放|重置|縮放重置 </span> </p> </td> 
   <td colname="col2"> <p> 配置按一下/點擊的映射以縮放操作。設定為 <span class="codeph"> 無 </span> 禁用按一下/點擊縮放。 如果設定為 <span class="codeph"> 縮放 </span> 按一下影像可縮放一個縮放步驟；CTRL+按一下可縮小一個縮放步驟。 設定為 <span class="codeph"> 重置 </span> 使按一下影像將縮放重置為初始縮放級別。 對於 <span class="codeph"> 縮放重置 </span>，如果當前縮放因子達到或超過指定限制，則應用重置，否則應用縮放。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-50bcd15223174bb79ce08b31ea03d682}

選填。

## 預設 {#section-7564169749ff4a4996049ea1148cb2a5}

`zoomReset` 在台式電腦上； `none` 觸摸設備。

## 範例 {#section-96e69b70365f461dae4399e49044ea2f}

`singleclick=zoom`
