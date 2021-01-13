---
description: PageView.singleclick
solution: Experience Manager
title: PageView.singleclick
topic: Dynamic media
uuid: 608700d2-5be4-4b96-b026-b12a3ade68ee
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 4%

---


# PageView.singleclick{#pageview-singleclick}

`[PageView.|<containerId>_pageView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_5654736F216D4ABC9FC783F83E0BBA03"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset  </span> </p> </td> 
   <td colname="col2"> <p> 設定單鍵／點選對應至縮放動作。設為<span class="codeph">無</span>會停用單鍵／點選縮放。 如果設定為<span class="codeph">縮放</span>，按一下影像會縮放一個縮放步驟；CTRL+Click可縮小一個縮放步驟。 設為<span class="codeph">重設</span>會讓您按一下影像，將縮放重設為初始縮放等級。 對於<span class="codeph"> zoomReset </span>，如果目前的縮放系數達到或超過指定的限制，則會套用重設，否則會套用縮放。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-edcfcd6c0bd24ac093442c56450b3c97}

選填。

## 預設 {#section-58cbfe8a90214c49bbbfb7e83c569d75}

`zoomReset` 在桌上型電腦上； `none` 觸控式裝置。

## 範例 {#section-5f63781afec94e0189e135995f686c20}

`singleclick=zoom`
