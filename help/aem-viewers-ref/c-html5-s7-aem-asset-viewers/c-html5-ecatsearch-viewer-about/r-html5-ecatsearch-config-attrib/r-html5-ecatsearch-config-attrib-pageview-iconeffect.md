---
description: 'null'
seo-description: 'null'
seo-title: PageView.iconEffect
solution: Experience Manager
title: PageView.iconEffect
topic: Dynamic media
uuid: c8d63ad9-6867-4b90-a113-6a75e394f706
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4

---


# PageView.iconEffect{#pageview-iconeffect}

[!DNL `[PageView.|<containerId>_pageView.]iconeffect=0|1[, *`countfadeauto`*][, *``*][, *`隱藏`*]`]

<table id="table_DD66FFC263A34220876DD204BFE62D49"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> 當影像 <span class="codeph"> 處於重設狀態時</span> ，可讓影像效果顯示在影像的頂端，並暗示可與影像互動的可用動作。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 計數</span></span> </p> </td> 
   <td colname="col2"> <p> 指定圖示效果出現和重 <span class="codeph"> 新顯示</span> 的最大次數。 值-1表 <span class="codeph"> 示圖</span> 示永遠會無限期地重新顯示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 淡化</span></span> </p> </td> 
   <td colname="col2"> <p>指定顯示或隱藏動畫的持續時間（以秒為單位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> autoHide</span></span> </p> </td> 
   <td colname="col2"> <p>設定在自動隱藏前， <span class="codeph"> iconeffect保持完全可見</span> 的秒數。 也就是說，淡入動畫完成後，淡出動畫開始之前的時間。 設定為 <span class="codeph"> 0</span> 會停用自動隱藏行為。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-b6e5e52698d4492f9d6350e7e312bb1b}

選填。

## 預設 {#section-7d0fc8fa09b34c288ed32ef7faa84604}

[!DNL `1,1,0.3,3`]

## 範例 {#section-95db1bfcccf241089654363203b19977}

[!DNL `iconeffect=0`]
