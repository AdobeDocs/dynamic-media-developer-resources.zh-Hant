---
description: ZoomView.singleclick
solution: Experience Manager
title: ZoomView.singleclick
feature: Dynamic Media Classic，檢視器，SDK/API，縮放
role: Developer,User
exl-id: c2292b5b-5b4e-4368-9495-9108042ec2f1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 4%

---

# ZoomView.singleclick{#zoomview-singleclick}

`[ZoomView.|<containerId>_zoomView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 無|縮放|重設|縮放重設  </span> </p> </td> 
   <td colname="col2"> <p> 設定單按/點選的對應以縮放動作。設為<span class="codeph"> none </span>會停用單按/點選縮放。 如果設為<span class="codeph">縮放</span>按一下影像會縮放一個縮放步驟；按住CTRL鍵並按一下可縮小一個縮放步驟。 將設定為<span class="codeph">重設</span>會導致在影像上按一下，將縮放重設為初始縮放等級。 對於<span class="codeph"> zoomReset </span>，如果當前縮放系數達到或超過指定限制，則應用重置，否則應用縮放。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-50bcd15223174bb79ce08b31ea03d682}

選填。

## 預設 {#section-7564169749ff4a4996049ea1148cb2a5}

`zoomReset` 在台式電腦上； `none` 在觸控裝置上。

## 範例 {#section-96e69b70365f461dae4399e49044ea2f}

`singleclick=zoom`
