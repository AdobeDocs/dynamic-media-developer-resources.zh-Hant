---
description: PageView.doubleclick
solution: Experience Manager
title: PageView.doubleclick
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: e6baef83-b4a8-4bef-bb13-263f3875030d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 3%

---

# PageView.doubleclick{#pageview-doubleclick}

[!DNL `[PageView.|<containerId>_pageView.]doubleclick=none|zoom|reset|zoomReset`]

<table id="table_942C8BDBDE1B441596987E9E971202E7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> 設定按兩下/點選以縮放動作的對應。 設定為<span class="codeph">無</span>會停用按兩下/點選縮放。 若設為<span class="codeph">縮放</span>，按一下影像可放大一個步階單位；按住Ctrl鍵並按一下滑鼠可縮小一個步階單位。 設定為<span class="codeph">重設</span>會導致按一下影像即可將縮放重設為初始縮放等級。 對於<span class="codeph"> zoomReset </span>，如果目前縮放因數達到或超過指定限制，則會套用重設，否則會套用縮放。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-03b915a16cf943afadc1bbaa4ef8e2eb}

選擇性.

## 預設 {#section-814d6bc6a0834005a0a72c7040e45693}

案頭電腦上的[!DNL `reset`]；觸控裝置上的[!DNL `zoomReset`]。

## 範例 {#section-986e7672f3694b7aa7572fb4428172ca}

[!DNL `doubleclick=zoom`]
