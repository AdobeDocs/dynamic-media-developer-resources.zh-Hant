---
description: PageView.frametransition
solution: Experience Manager
title: PageView.frametransition
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 19239fa8-65a8-487f-9370-42bb93d862d5
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 4%

---

# PageView.frametransition{#pageview-frametransition}

[!DNL ` [PageView.|<containerId>_pageView.]frametransition=slide|turn|auto[, *`時段`*]`]

<table id="table_625D0EEDA21B46FEA3F5CF7DDF769B50"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幻燈片|轉彎|自動</span> </p> </td> 
   <td colname="col2"> <p> 指定應用於幀更改的效果類型。 </p> <p> 
     <ul id="ul_4224B7C2722A4185A8BD48703D019AA1"> 
      <li id="li_8482037F8E1C4F11A84DF51790A073FE"> <p><span class="codeph"> 滑</span> 激活一個過渡，其中舊框架滑出視圖，而新框架滑入到視圖。 </p> </li> 
      <li id="li_CE9A99564DF348D0A76AB2A5945155A5"> <p><span class="codeph"> 轉</span> 當用戶可以拖動四個跨頁角之一併執行互動式翻頁時，啟用翻頁效果。 </p> <p>當 <span class="codeph"> 轉</span> 使用 <span class="codeph"> 翻頁</span> 修飾符和 <span class="codeph"> .s7分頁符</span> 忽略CSS類。 </p> <p>注意：  <p><span class="codeph"> 轉</span> Motorola Xoom不支援動畫。 </p> </p> </li> 
      <li id="li_79F85B0429CD4B389399FB3823FE767F"> <p> <span class="codeph"> 自動</span> 設定台式機系統的轉彎框架過渡和觸摸設備上的幻燈片過渡。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 時段</span></span> </p> </td> 
   <td colname="col2"> <p>指定持續時間（秒） <span class="codeph"> 滑</span> 或 <span class="codeph"> 轉</span> 過渡效果。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-4d25a3f483834d2b9586fa70270ce6bd}

選擇性.

## 預設 {#section-d677f04f1c894966884ce9d77a5ea1c1}

[!DNL `slide,0.3`]

## 範例 {#section-b877011e5f6240718e9451be8f622c02}

[!DNL `frametransition=auto,1`]
