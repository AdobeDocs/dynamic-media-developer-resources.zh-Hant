---
title: PageView.singleclick
description: PageView.singleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 96896145-f8d9-4fee-abfe-7f9193776993
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# PageView.singleclick{#pageview-singleclick}

`[PageView.|<containerId>_pageView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_5654736F216D4ABC9FC783F83E0BBA03"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 無|縮放|重設|縮放重設 </span> </p> </td> 
   <td colname="col2"> <p> 設定單按/點選的對應以縮放動作。設定為 <span class="codeph"> 無 </span> 停用單按/點選縮放。 若設為 <span class="codeph"> 縮放 </span> 按一下影像會在一個縮放步驟中縮放；按住CTRL鍵並按一下可縮小一個縮放步驟。 設定為 <span class="codeph"> 重設 </span> 會導致在影像上按一下，將縮放重設為初始縮放等級。 針對 <span class="codeph"> zoomReset </span>，則當前縮放系數在指定限制或超過指定限制時，會套用重設，否則會套用縮放。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-edcfcd6c0bd24ac093442c56450b3c97}

選填。

## 預設 {#section-58cbfe8a90214c49bbbfb7e83c569d75}

`zoomReset` 在台式電腦上； `none` 在觸控裝置上。

## 範例 {#section-5f63781afec94e0189e135995f686c20}

`singleclick=zoom`
