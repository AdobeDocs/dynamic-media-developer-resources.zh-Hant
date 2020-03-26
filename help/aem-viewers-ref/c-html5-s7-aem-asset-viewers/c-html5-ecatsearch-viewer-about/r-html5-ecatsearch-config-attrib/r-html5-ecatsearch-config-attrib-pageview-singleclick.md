---
description: 'null'
seo-description: 'null'
seo-title: PageView.synclick
solution: Experience Manager
title: PageView.synclick
topic: Dynamic media
uuid: b08b605e-5ffc-42cc-931d-d67750a8dca8
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4

---


# PageView.synclick{#pageview-singleclick}

[!DNL `[PageView.|<containerId>_pageView.]singleclick=none|zoom|reset|zoomReset`]

<table id="table_5654736F216D4ABC9FC783F83E0BBA03"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> 設定單鍵／點選對應至縮放動作。設定為無 <span class="codeph"> 會停 </span> 用單鍵／點選縮放。 如果設定縮放 <span class="codeph"> 功能， </span> 按一下影像會縮放一個縮放步驟；CTRL+Click可縮小一個縮放步驟。 設定為 <span class="codeph"> 重設 </span> 會導致在影像上按一下，將縮放重設為初始縮放等級。 對於 <span class="codeph"> 縮放重 </span>設，如果目前的縮放比例達到或超過指定的限制，則會套用重設，否則會套用縮放。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-edcfcd6c0bd24ac093442c56450b3c97}

選填。

## 預設 {#section-58cbfe8a90214c49bbbfb7e83c569d75}

[!DNL `zoomReset`] 在桌上型電腦上；觸 [!DNL `none`] 控裝置。

## 範例 {#section-5f63781afec94e0189e135995f686c20}

[!DNL `singleclick=zoom`]