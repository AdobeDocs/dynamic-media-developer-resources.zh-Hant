---
title: PageView.frametransition
description: PageView.frametransition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 026c2fc5-0460-481c-aca9-ddd25371779c
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 3%

---

# PageView.frametransition{#pageview-frametransition}

` [PageView.|<containerId>_pageView.]frametransition=slide|turn|auto[, *`持續時間`*]`

<table id="table_625D0EEDA21B46FEA3F5CF7DDF769B50"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">張投影片|翻轉|自動</span> </p> </td> 
   <td colname="col2"> <p> 指定套用到影格變更的效果型別。 </p> <p> 
     <ul id="ul_4224B7C2722A4185A8BD48703D019AA1"> 
      <li id="li_8482037F8E1C4F11A84DF51790A073FE"> <p><span class="codeph">張投影片</span>會啟動舊框架滑出檢視，新框架滑入檢視的轉變。 </p> </li> 
      <li id="li_CE9A99564DF348D0A76AB2A5945155A5"> <p><span class="codeph">翻轉</span>啟用頁面翻轉效果，使用者可以拖曳四個試算表之一并執行互動式頁面翻轉。 </p> <p>使用<span class="codeph"> turn</span>時，元件的外觀是由<span class="codeph"> pageturnstyle</span>修飾元所控制，且會忽略<span class="codeph"> .s7pagedider</span> CSS類別。 </p> <p>注意：  <p>摩托羅拉Xoom不支援<span class="codeph">翻轉</span>動畫。 </p> </p> </li> 
      <li id="li_79F85B0429CD4B389399FB3823FE767F"> <p> <span class="codeph"> auto</span>設定案頭系統上的翻頁影格切換，以及觸控裝置上的投影片切換。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname">持續時間</span></span> </p> </td> 
   <td colname="col2"> <p>指定<span class="codeph">投影片</span>或<span class="codeph">翻轉</span>轉換效果的持續時間（以秒為單位）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-4d25a3f483834d2b9586fa70270ce6bd}

選擇性.

## 預設 {#section-d677f04f1c894966884ce9d77a5ea1c1}

`slide,0.3`

## 範例 {#section-b877011e5f6240718e9451be8f622c02}

`frametransition=auto,1`
