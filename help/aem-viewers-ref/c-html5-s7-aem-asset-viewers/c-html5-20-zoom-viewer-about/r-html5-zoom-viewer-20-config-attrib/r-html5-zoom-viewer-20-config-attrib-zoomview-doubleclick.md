---
description: ZoomView.doubleclick
solution: Experience Manager
title: ZoomView.doubleclick
feature: Dynamic Media Classic，檢視器，SDK/API，縮放
role: Developer,User
exl-id: 9f52542e-398c-45a2-89ea-95c9aefbde3e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 4%

---

# ZoomView.doubleclick{#zoomview-doubleclick}

`[ZoomView.|<containerId>_zoomView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 無|縮放|重設|縮放重設  </span> </p> </td> 
   <td colname="col2"> <p> 設定按兩下/點選以縮放動作的對應。 設為<span class="codeph"> none </span>會停用按兩下/點選縮放。 如果設為<span class="codeph">縮放</span>按一下影像會縮放一個縮放步驟；按住CTRL鍵並按一下可縮小一個縮放步驟。 將設定為<span class="codeph">重設</span>會導致在影像上按一下，將縮放重設為初始縮放等級。 對於<span class="codeph"> zoomReset </span>，如果當前縮放系數達到或超過指定限制，則應用重置，否則應用縮放。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

選填。

## 預設 {#section-71fb773f814649b2885aefee68073641}

`reset` 在台式電腦上； `zoomReset` 在觸控裝置上。

## 範例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`doubleclick=zoom`
