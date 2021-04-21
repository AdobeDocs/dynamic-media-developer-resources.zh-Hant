---
description: PageView.frametransition
solution: Experience Manager
title: PageView.frametransition
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 5%

---


# PageView.frametransition{#pageview-frametransition}

[!DNL ` [PageView.|<containerId>_pageView.]frametransition=slide|turn|auto[, *`時段`*]`]

<table id="table_625D0EEDA21B46FEA3F5CF7DDF769B50"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> slide|turn|auto</span> </p> </td> 
   <td colname="col2"> <p> 指定在影格變更上套用的效果類型。 </p> <p> 
     <ul id="ul_4224B7C2722A4185A8BD48703D019AA1"> 
      <li id="li_8482037F8E1C4F11A84DF51790A073FE"> <p><span class="codeph"> 投</span> 影片會啟動轉場，舊影格會滑出檢視，新影格則會滑入檢視。 </p> </li> 
      <li id="li_CE9A99564DF348D0A76AB2A5945155A5"> <p><span class="codeph"> 當使</span> 用者可以拖曳四個跨頁轉角之一，並執行互動式頁面翻轉時，就會啟用頁面翻轉效果。 </p> <p>當使用<span class="codeph"> turn</span>時，會使用<span class="codeph"> pageturnstyle</span>修飾元控制元件的外觀，並忽略<span class="codeph"> .s7pagedifer</span> CSS類別。 </p> <p>注意：  <p><span class="codeph"> Motorola </span> Xoom不支援突變。 </p> </p> </li> 
      <li id="li_79F85B0429CD4B389399FB3823FE767F"> <p> <span class="codeph"> 在桌</span> 上型電腦系統上自動設定轉動影格轉換，在觸控裝置上自動設定投影片轉換。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 時段</span></span> </p> </td> 
   <td colname="col2"> <p>指定<span class="codeph">投影片</span>或<span class="codeph"> turn</span>轉場效果的持續時間（秒）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-4d25a3f483834d2b9586fa70270ce6bd}

選填。

## 預設 {#section-d677f04f1c894966884ce9d77a5ea1c1}

[!DNL `slide,0.3`]

## 範例 {#section-b877011e5f6240718e9451be8f622c02}

[!DNL `frametransition=auto,1`]
