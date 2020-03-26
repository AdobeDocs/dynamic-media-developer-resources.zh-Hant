---
description: 'null'
seo-description: 'null'
seo-title: SpinView.synclick
solution: Experience Manager
title: SpinView.synclick
topic: Dynamic media
uuid: 188a4e65-a93e-46c4-89b4-02e745ecf5eb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SpinView.synclick{#spinview-singleclick}

`[SpinView.|<containerId>_spinView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_0824E332DF1340A2ABC40A3EB428F2D0"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> 設定單鍵／點選對應至縮放動作。設定為無 <span class="codeph"> 會停 </span> 用單鍵／點選縮放。 如果設定縮放 <span class="codeph"> 功能， </span> 按一下影像會縮放一個縮放步驟；CTRL+Click可縮小一個縮放步驟。 若設定為 <span class="codeph"> 重設， </span> 只要按一下影像，就會將縮放重設為初始回轉等級。 對於 <span class="codeph"> 縮放重 </span>設，如果目前的縮放比例達到或超過指定的限制，則會套用重設，否則會套用縮放。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

選填。

## 預設 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`zoomReset` 在桌上型電腦上；觸 `none` 控裝置。

## 範例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`singleclick=zoom`
