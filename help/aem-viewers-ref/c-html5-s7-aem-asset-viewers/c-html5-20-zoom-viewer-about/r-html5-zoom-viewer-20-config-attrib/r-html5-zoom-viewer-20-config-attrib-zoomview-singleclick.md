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
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> 設定按一下/點選以縮放動作的對應。 設定為<span class="codeph">無</span>會停用按一下/點選縮放。 若設為<span class="codeph">縮放</span>，按一下影像可放大一個步階單位；按住Ctrl鍵並按一下滑鼠可縮小一個步階單位。 設定為<span class="codeph">重設</span>會導致按一下影像即可將縮放重設為初始縮放等級。 對於<span class="codeph"> zoomReset </span>，如果目前縮放因數達到或超過指定限制，則會套用重設，否則會套用縮放。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

選擇性.

## 預設 {#section-71fb773f814649b2885aefee68073641}

`zoomReset` — 在桌上型電腦上； `none`在觸控裝置上。

## 範例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`singleclick=zoom`
