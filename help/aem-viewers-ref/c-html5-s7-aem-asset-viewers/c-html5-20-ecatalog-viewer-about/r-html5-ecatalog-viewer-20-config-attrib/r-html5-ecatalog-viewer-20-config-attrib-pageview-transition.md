---
title: PageView.transition
description: PageView.transition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: aa12a210-88d9-4b96-b598-6967496ac668
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# PageView.transition{#pageview-transition}

` [PageView.|<containerId>_pageView.]transition= *`時間`*[, *`寬鬆`*]`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 時間</span></span> </p> </td> 
   <td colname="col2"> <p> 指定單縮放步驟操作的動畫所花費的秒數。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 寬鬆</span></span> </p> </td> 
   <td colname="col2"> <p> 建立加速或減速的假象，使轉變更自然。 您可以將緩動設為下列其中一個項目： </p> <p> 
     <ul id="ul_DA0D1CF2F2484410BFCCACA86661702E"> 
      <li id="li_93A2D53A53314D9594CEDC9EB20381D4">0（自動） </li> 
      <li id="li_AD6A1F03DE544959BC4AA0DD97494F8C"> 1（線性） </li> 
      <li id="li_816A3CE796E3415B9650DDA204412A6A"> 2（二次） </li> 
      <li id="li_EF00BF6CA2AA48FEB54015FFBA9F8DD4"> 3（立方） </li> 
      <li id="li_F3CB7F0821AF489C84A0CA155F5031A2"> 4（四分位） </li> 
      <li id="li_F5B844DAF4CC453CA58BF09A660D139F"> 5（五次） </li> 
     </ul> </p> <p>停用彈性縮放時（預設值），「自動」模式一律使用線性轉變。 否則，它適合基於轉變時間的其他緩動功能之一。 即，過渡時間越短，加速或減速效果的加緩函式就越大。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-ebfd9162c8504666bf0e4485bf3b1383}

選填。

## 預設 {#section-9f91ce6567384ab691e4d4f8a7015455}

`0.5,0`

## 範例 {#section-cb6b8793ee9946b8bf1cfddab8612db5}

`transition=2,2`
