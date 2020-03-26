---
description: 'null'
seo-description: 'null'
seo-title: SpinView.synclick
solution: Experience Manager
title: SpinView.synclick
topic: Dynamic media
uuid: b360db52-f705-4966-b77b-009bed729c25
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SpinView.synclick{#spinview-singleclick}

`[SpinView.|<containerId>_spinView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> 設定單鍵／點選對應至縮放動作。設定為無 <span class="codeph"> 會停 </span> 用單鍵／點選縮放。 如果設為旋轉 <span class="codeph"> 按一 </span> 下影像，會在一個縮放步驟中縮放；CTRL+Click可縮小一個縮放步驟。 若設定為 <span class="codeph"> 重設， </span> 只要按一下影像，就會將縮放重設為初始回轉等級。 對於 <span class="codeph"> 縮放重 </span>設，如果目前的縮放比例達到或超過指定的限制，則會套用重設，否則會套用縮放。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-924163cb2f6542499f49894becef7fb5}

選填。

## 預設 {#section-7a2128fd488941948aff18421f533ccf}

`zoomReset` 在桌上型電腦上；觸 `none` 控裝置。

## 範例 {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`singleclick=zoom`
