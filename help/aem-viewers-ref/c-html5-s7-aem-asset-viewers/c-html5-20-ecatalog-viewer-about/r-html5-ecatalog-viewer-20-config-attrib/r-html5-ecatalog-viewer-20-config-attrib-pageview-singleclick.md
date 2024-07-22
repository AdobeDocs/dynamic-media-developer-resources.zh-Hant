---
title: PageView.singleclick
description: PageView.singleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 96896145-f8d9-4fee-abfe-7f9193776993
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 3%

---

# PageView.singleclick{#pageview-singleclick}

`[PageView.|<containerId>_pageView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_5654736F216D4ABC9FC783F83E0BBA03"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> 設定按一下/點選以縮放動作的對應。 設定為<span class="codeph">無</span>會停用按一下/點選縮放。 若設為<span class="codeph">縮放</span>，按一下影像可放大一個步階單位；按住Ctrl鍵並按一下滑鼠可縮小一個步階單位。 設定為<span class="codeph">重設</span>會導致按一下影像即可將縮放重設為初始縮放等級。 對於<span class="codeph"> zoomReset </span>，如果目前縮放因數達到或超過指定限制，則會套用重設，否則會套用縮放。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-edcfcd6c0bd24ac093442c56450b3c97}

選擇性.

## 預設 {#section-58cbfe8a90214c49bbbfb7e83c569d75}

案頭電腦上的`zoomReset`；觸控裝置上的`none`。

## 範例 {#section-5f63781afec94e0189e135995f686c20}

`singleclick=zoom`
