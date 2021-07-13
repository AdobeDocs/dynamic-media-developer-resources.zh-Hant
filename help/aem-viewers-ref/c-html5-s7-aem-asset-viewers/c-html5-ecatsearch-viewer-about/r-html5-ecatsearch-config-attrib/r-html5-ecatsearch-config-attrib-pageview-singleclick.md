---
description: PageView.singleclick
solution: Experience Manager
title: PageView.singleclick
feature: Dynamic Media Classic，檢視器，SDK/API,eCatalog搜尋
role: Developer,User
exl-id: ffe77be7-bf12-4e9d-9355-2857d366d14e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 4%

---

# PageView.singleclick{#pageview-singleclick}

[!DNL `[PageView.|<containerId>_pageView.]singleclick=none|zoom|reset|zoomReset`]

<table id="table_5654736F216D4ABC9FC783F83E0BBA03"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 無|縮放|重設|縮放重設  </span> </p> </td> 
   <td colname="col2"> <p> 設定單按/點選的對應以縮放動作。設為<span class="codeph"> none </span>會停用單按/點選縮放。 如果設為<span class="codeph">縮放</span>按一下影像會縮放一個縮放步驟；按住CTRL鍵並按一下可縮小一個縮放步驟。 將設定為<span class="codeph">重設</span>會導致在影像上按一下，將縮放重設為初始縮放等級。 對於<span class="codeph"> zoomReset </span>，如果當前縮放系數達到或超過指定限制，則應用重置，否則應用縮放。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-edcfcd6c0bd24ac093442c56450b3c97}

選填。

## 預設 {#section-58cbfe8a90214c49bbbfb7e83c569d75}

[!DNL `zoomReset`] 在台式電腦上； [!DNL `none`] 在觸控裝置上。

## 範例 {#section-5f63781afec94e0189e135995f686c20}

[!DNL `singleclick=zoom`]
