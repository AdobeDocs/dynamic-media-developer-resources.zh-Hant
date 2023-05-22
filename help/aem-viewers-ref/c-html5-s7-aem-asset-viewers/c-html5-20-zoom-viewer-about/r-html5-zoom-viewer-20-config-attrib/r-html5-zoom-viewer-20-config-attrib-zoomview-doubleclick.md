---
title: ZoomView.doubleclick
description: ZoomView.doubleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 9f52542e-398c-45a2-89ea-95c9aefbde3e
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 3%

---

# ZoomView.doubleclick{#zoomview-doubleclick}

`[ZoomView.|<containerId>_zoomView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 無|縮放|重置|縮放重置 </span> </p> </td> 
   <td colname="col2"> <p> 配置按兩下/點擊以縮放操作的映射。 設定為 <span class="codeph"> 無 </span> 禁用按兩下/點擊縮放。 如果設定為 <span class="codeph"> 縮放 </span> 按一下影像可縮放一個縮放步驟；CTRL+按一下可縮小一個縮放步驟。 設定為 <span class="codeph"> 重置 </span> 使按一下影像將縮放重置為初始縮放級別。 對於 <span class="codeph"> 縮放重置 </span>，如果當前縮放因子達到或超過指定限制，則應用重置，否則應用縮放。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

選擇性.

## 預設 {#section-71fb773f814649b2885aefee68073641}

`reset`  — 在台式電腦上； `zoomReset` 觸摸設備。

## 範例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`doubleclick=zoom`
