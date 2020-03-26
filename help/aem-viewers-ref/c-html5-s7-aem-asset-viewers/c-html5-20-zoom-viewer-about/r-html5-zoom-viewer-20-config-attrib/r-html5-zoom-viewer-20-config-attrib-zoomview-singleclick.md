---
description: 'null'
seo-description: 'null'
seo-title: ZoomView.synclick
solution: Experience Manager
title: ZoomView.synclick
topic: Dynamic media
uuid: 919dd48e-b621-4dbb-9cae-f2d0f91f45a9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ZoomView.synclick{#zoomview-singleclick}

`[ZoomView.|<containerId>_zoomView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> 設定單鍵／點選對應至縮放動作。設定為無 <span class="codeph"> 會停 </span> 用單鍵／點選縮放。 如果設定縮放 <span class="codeph"> 功能， </span> 按一下影像會縮放一個縮放步驟；CTRL+Click可縮小一個縮放步驟。 設定為 <span class="codeph"> 重設 </span> 會導致在影像上按一下，將縮放重設為初始縮放等級。 對於 <span class="codeph"> 縮放重 </span>設，如果目前的縮放比例達到或超過指定的限制，則會套用重設，否則會套用縮放。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

選填。

## 預設 {#section-71fb773f814649b2885aefee68073641}

`zoomReset` 在桌上型電腦上；觸 `none` 控裝置。

## 範例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`singleclick=zoom`
