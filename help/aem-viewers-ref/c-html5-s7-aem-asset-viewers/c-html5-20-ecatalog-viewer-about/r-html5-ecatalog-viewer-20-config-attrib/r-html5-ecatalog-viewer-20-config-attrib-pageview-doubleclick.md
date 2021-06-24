---
description: PageView.doubleclick
solution: Experience Manager
title: PageView.doubleclick
feature: Dynamic Media Classic，檢視器，SDK/API,eCatalog
role: Developer,Business Practitioner
exl-id: d53a8723-d710-4722-b1a7-c88d3b9d270b
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 4%

---

# PageView.doubleclick{#pageview-doubleclick}

`[PageView.|<containerId>_pageView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_942C8BDBDE1B441596987E9E971202E7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 無|縮放|重設|縮放重設  </span> </p> </td> 
   <td colname="col2"> <p> 設定按兩下/點選以縮放動作的對應。 設為<span class="codeph"> none </span>會停用按兩下/點選縮放。 如果設為<span class="codeph">縮放</span>按一下影像會縮放一個縮放步驟；按住CTRL鍵並按一下可縮小一個縮放步驟。 將設定為<span class="codeph">重設</span>會導致在影像上按一下，將縮放重設為初始縮放等級。 對於<span class="codeph"> zoomReset </span>，如果當前縮放系數達到或超過指定限制，則應用重置，否則應用縮放。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-03b915a16cf943afadc1bbaa4ef8e2eb}

選填。

## 預設 {#section-814d6bc6a0834005a0a72c7040e45693}

`reset` 在台式電腦上； `zoomReset` 在觸控裝置上。

## 範例 {#section-986e7672f3694b7aa7572fb4428172ca}

`doubleclick=zoom`
