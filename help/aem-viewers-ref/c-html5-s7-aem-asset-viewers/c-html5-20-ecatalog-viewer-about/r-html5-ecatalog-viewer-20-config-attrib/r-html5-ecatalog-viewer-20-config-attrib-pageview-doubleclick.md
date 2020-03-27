---
description: 'null'
seo-description: 'null'
seo-title: PageView.doubleclick
solution: Experience Manager
title: PageView.doubleclick
topic: Dynamic media
uuid: ac4fb532-f554-4831-b341-7f8d6ef3a1c0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# PageView.doubleclick{#pageview-doubleclick}

`[PageView.|<containerId>_pageView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_942C8BDBDE1B441596987E9E971202E7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> 設定按兩下／點選以縮放動作的對應。 設定為 <span class="codeph"> 無 </span> 會停用雙按／點選縮放。 如果設定縮放 <span class="codeph"> 功能， </span> 按一下影像會縮放一個縮放步驟；CTRL+Click可縮小一個縮放步驟。 設定為 <span class="codeph"> 重設 </span> 會導致在影像上按一下，將縮放重設為初始縮放等級。 對於 <span class="codeph"> 縮放重 </span>設，如果目前的縮放比例達到或超過指定的限制，則會套用重設，否則會套用縮放。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-03b915a16cf943afadc1bbaa4ef8e2eb}

選填。

## 預設 {#section-814d6bc6a0834005a0a72c7040e45693}

`reset` 在桌上型電腦上；觸 `zoomReset` 控裝置。

## 範例 {#section-986e7672f3694b7aa7572fb4428172ca}

`doubleclick=zoom`
