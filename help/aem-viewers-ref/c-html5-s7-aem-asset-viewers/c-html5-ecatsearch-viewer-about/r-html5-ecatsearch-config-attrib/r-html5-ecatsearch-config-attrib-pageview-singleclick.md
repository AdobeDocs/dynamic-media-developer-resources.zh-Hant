---
description: PageView.singleclick
solution: Experience Manager
title: PageView.singleclick
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 3%

---


# PageView.singleclick{#pageview-singleclick}

[!DNL `[PageView.|<containerId>_pageView.]singleclick=none|zoom|reset|zoomReset`]

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

[!DNL `zoomReset`] 在桌上型電腦上； [!DNL `none`] 觸控式裝置。

## 範例 {#section-5f63781afec94e0189e135995f686c20}

[!DNL `singleclick=zoom`]