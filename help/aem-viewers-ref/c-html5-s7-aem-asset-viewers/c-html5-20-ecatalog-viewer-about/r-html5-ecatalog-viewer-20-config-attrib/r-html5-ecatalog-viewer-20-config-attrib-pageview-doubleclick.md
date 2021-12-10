---
title: PageView.doubleclick
description: PageView.doubleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: d53a8723-d710-4722-b1a7-c88d3b9d270b
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 4%

---

# PageView.doubleclick{#pageview-doubleclick}

`[PageView.|<containerId>_pageView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_942C8BDBDE1B441596987E9E971202E7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 無|縮放|重設|縮放重設 </span> </p> </td> 
   <td colname="col2"> <p> 設定按兩下/點選以縮放動作的對應。 設定為 <span class="codeph"> 無 </span> 停用按兩下/點選縮放。 若設為 <span class="codeph"> 縮放 </span> 按一下影像會在一個縮放步驟中縮放；按住CTRL鍵並按一下可縮小一個縮放步驟。 設定為 <span class="codeph"> 重設 </span> 會導致在影像上按一下，將縮放重設為初始縮放等級。 針對 <span class="codeph"> zoomReset </span>，則當前縮放系數在指定限制或超過指定限制時，會套用重設，否則會套用縮放。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-03b915a16cf943afadc1bbaa4ef8e2eb}

選填。

## 預設 {#section-814d6bc6a0834005a0a72c7040e45693}

`reset` 在台式電腦上； `zoomReset` 在觸控裝置上。

## 範例 {#section-986e7672f3694b7aa7572fb4428172ca}

`doubleclick=zoom`
