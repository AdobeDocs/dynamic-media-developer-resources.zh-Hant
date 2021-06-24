---
description: PageView.frametransition
solution: Experience Manager
title: PageView.frametransition
feature: Dynamic Media Classic，檢視器，SDK/API,eCatalog搜尋
role: Developer,Business Practitioner
exl-id: 19239fa8-65a8-487f-9370-42bb93d862d5
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 5%

---

# PageView.frametransition{#pageview-frametransition}

[!DNL ` [PageView.|<containerId>_pageView.]frametransition=slide|turn|auto[, *`時段`*]`]

<table id="table_625D0EEDA21B46FEA3F5CF7DDF769B50"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幻燈片|turn|auto</span> </p> </td> 
   <td colname="col2"> <p> 指定對幀更改應用的效果類型。 </p> <p> 
     <ul id="ul_4224B7C2722A4185A8BD48703D019AA1"> 
      <li id="li_8482037F8E1C4F11A84DF51790A073FE"> <p><span class="codeph"> </span> 投影片會啟動一個轉變，舊框架滑出視圖，新框架滑入到視圖中。 </p> </li> 
      <li id="li_CE9A99564DF348D0A76AB2A5945155A5"> <p><span class="codeph"> </span> 當使用者可拖曳四個跨頁角之一併執行互動式頁面翻轉時，就會啟用頁面翻轉效果。 </p> <p>使用<span class="codeph"> turn</span>時，使用<span class="codeph"> pageturnstyle</span>修飾符控制元件的外觀，並忽略<span class="codeph"> .s7pagedifer</span> CSS類。 </p> <p>注意：  <p><span class="codeph"> </span> Motorola Xoom不支援轉換。 </p> </p> </li> 
      <li id="li_79F85B0429CD4B389399FB3823FE767F"> <p> <span class="codeph"> </span> 會在案頭系統上自動設定轉彎框架過渡，並在觸控裝置上自動設定滑動過渡。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 時段</span></span> </p> </td> 
   <td colname="col2"> <p>指定<span class="codeph">幻燈片</span>或<span class="codeph">轉</span>轉變效果的持續時間（秒）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-4d25a3f483834d2b9586fa70270ce6bd}

選填。

## 預設 {#section-d677f04f1c894966884ce9d77a5ea1c1}

[!DNL `slide,0.3`]

## 範例 {#section-b877011e5f6240718e9451be8f622c02}

[!DNL `frametransition=auto,1`]
