---
description: PageView.doubleclick
solution: Experience Manager
title: PageView.doubleclick
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 3%

---


# PageView.doubleclick{#pageview-doubleclick}

[!DNL `[PageView.|<containerId>_pageView.]doubleclick=none|zoom|reset|zoomReset`]

<table id="table_942C8BDBDE1B441596987E9E971202E7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset  </span> </p> </td> 
   <td colname="col2"> <p> 設定按兩下／點選以縮放動作的對應。 設為<span class="codeph"> none </span>會停用按兩下／點選縮放。 如果設定為<span class="codeph">縮放</span>，按一下影像會縮放一個縮放步驟；CTRL+Click可縮小一個縮放步驟。 設為<span class="codeph">重設</span>會讓您按一下影像，將縮放重設為初始縮放等級。 對於<span class="codeph"> zoomReset </span>，如果目前的縮放系數達到或超過指定的限制，則會套用重設，否則會套用縮放。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-03b915a16cf943afadc1bbaa4ef8e2eb}

選填。

## 預設 {#section-814d6bc6a0834005a0a72c7040e45693}

[!DNL `reset`] 在桌上型電腦上； [!DNL `zoomReset`] 觸控式裝置。

## 範例 {#section-986e7672f3694b7aa7572fb4428172ca}

[!DNL `doubleclick=zoom`]
