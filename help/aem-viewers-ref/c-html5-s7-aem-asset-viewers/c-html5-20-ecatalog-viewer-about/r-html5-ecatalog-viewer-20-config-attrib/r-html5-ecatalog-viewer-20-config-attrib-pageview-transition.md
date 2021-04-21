---
description: PageView.transition
solution: Experience Manager
title: PageView.transition
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 4%

---


# PageView.transition{#pageview-transition}

` [PageView.|<containerId>_pageView.]transition= *`調`*[, *`整`*]`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 時間</span></span> </p> </td> 
   <td colname="col2"> <p> 指定單一縮放步驟動作的動畫所花的時間（以秒為單位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 寬鬆</span></span> </p> </td> 
   <td colname="col2"> <p> 產生加速或減速的錯覺，使轉場更自然。 您可以將加減速設定為以下任一選項： </p> <p> 
     <ul id="ul_DA0D1CF2F2484410BFCCACA86661702E"> 
      <li id="li_93A2D53A53314D9594CEDC9EB20381D4">0（自動） </li> 
      <li id="li_AD6A1F03DE544959BC4AA0DD97494F8C"> 1（線性） </li> 
      <li id="li_816A3CE796E3415B9650DDA204412A6A"> 2（二次） </li> 
      <li id="li_EF00BF6CA2AA48FEB54015FFBA9F8DD4"> 3（立方） </li> 
      <li id="li_F3CB7F0821AF489C84A0CA155F5031A2"> 4（四分位） </li> 
      <li id="li_F5B844DAF4CC453CA58BF09A660D139F"> 5（五分） </li> 
     </ul> </p> <p>在停用彈性縮放時，自動模式一律會使用線性轉場（預設）。 否則，它適合基於過渡時間的其它一種緩動功能。 即，過渡時間越短，加減速作用越強。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-ebfd9162c8504666bf0e4485bf3b1383}

選填。

## 預設 {#section-9f91ce6567384ab691e4d4f8a7015455}

`0.5,0`

## 範例 {#section-cb6b8793ee9946b8bf1cfddab8612db5}

`transition=2,2`
