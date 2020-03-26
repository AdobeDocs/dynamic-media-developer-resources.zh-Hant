---
description: 'null'
seo-description: 'null'
seo-title: ZoomView.doubleclick
solution: Experience Manager
title: ZoomView.doubleclick
topic: Dynamic media
uuid: 2f44dc7f-ebed-4c74-b1ea-0b65655059fe
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ZoomView.doubleclick{#zoomview-doubleclick}

`[ZoomView.|<containerId>_zoomView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> 設定按兩下／點選以縮放動作的對應。 設定為 <span class="codeph"> 無 </span> 會停用雙按／點選縮放。 如果設定縮放 <span class="codeph"> 功能， </span> 按一下影像會縮放一個縮放步驟；CTRL+Click可縮小一個縮放步驟。 設定為 <span class="codeph"> 重設 </span> 會導致在影像上按一下，將縮放重設為初始縮放等級。 對於 <span class="codeph"> 縮放重 </span>設，如果目前的縮放比例達到或超過指定的限制，則會套用重設，否則會套用縮放。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

選填。

## 預設 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`reset` 在桌上型電腦上；觸 `zoomReset` 控裝置。

## 範例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`doubleclick=zoom`
