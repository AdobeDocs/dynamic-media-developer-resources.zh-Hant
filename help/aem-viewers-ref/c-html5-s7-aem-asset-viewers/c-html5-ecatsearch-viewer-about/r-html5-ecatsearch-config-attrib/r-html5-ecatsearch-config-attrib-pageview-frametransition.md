---
description: 'null'
seo-description: 'null'
seo-title: PageView.frametransition
solution: Experience Manager
title: PageView.frametransition
topic: Dynamic media
uuid: 12595a89-bad5-4224-aeff-52ce6bb615ee
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4

---


# PageView.frametransition{#pageview-frametransition}

[!DNL ` [PageView.|<containerId>_pageView.]frametransition=slide|turn|auto[, *`時段`*]`]

<table id="table_625D0EEDA21B46FEA3F5CF7DDF769B50"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> slide|turn|auto</span> </p> </td> 
   <td colname="col2"> <p> 指定在影格變更上套用的效果類型。 </p> <p> 
     <ul id="ul_4224B7C2722A4185A8BD48703D019AA1"> 
      <li id="li_8482037F8E1C4F11A84DF51790A073FE"> <p><span class="codeph"> slide</span> 會啟動轉場，舊影格會滑出檢視，新影格則會滑入檢視。 </p> </li> 
      <li id="li_CE9A99564DF348D0A76AB2A5945155A5"> <p><span class="codeph"> turn</span> 可讓使用者拖曳四個跨頁轉角之一，並執行互動式頁面翻轉時，啟用頁面翻轉效果。 </p> <p>使用 <span class="codeph"> turn</span> 時，元件的外觀會使用pageturnstyle修飾元來控制 <span class="codeph"> ，而</span> .s7pagedifer <span class="codeph"></span> CSS類別則會被忽略。 </p> <p>注意：  <p><span class="codeph"> Motorola</span> Xoom不支援turn動畫。 </p> </p> </li> 
      <li id="li_79F85B0429CD4B389399FB3823FE767F"> <p> <span class="codeph"> 自動</span> ，在桌上型電腦系統上設定轉動影格切換效果，在觸控裝置上設定滑動切換效果。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 時段</span></span> </p> </td> 
   <td colname="col2"> <p>指定投影片或轉動轉場效果 <span class="codeph"> 的持</span><span class="codeph"> 續時間</span> （秒）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-4d25a3f483834d2b9586fa70270ce6bd}

選填。

## 預設 {#section-d677f04f1c894966884ce9d77a5ea1c1}

[!DNL `slide,0.3`]

## 範例 {#section-b877011e5f6240718e9451be8f622c02}

[!DNL `frametransition=auto,1`]
