---
description: 'null'
seo-description: 'null'
seo-title: ZoomView.transition
solution: Experience Manager
title: ZoomView.transition
topic: Dynamic media
uuid: f579397b-a449-42fe-b0a7-f0da65a6a248
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ZoomView.transition{#zoomview-transition}

` [ZoomView.|<containerId>_zoomView.]transition= *`調`*[, *`整`*]`

<table id="table_9E7BB12BF371419F88DD4D24EF04632C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 時 <span class="varname"> 間</span></span> </p> </td> 
   <td colname="col2"> <p> 指定單一縮放步驟動作的動畫所花的時間（以秒為單位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 緩 <span class="varname"> 動</span></span> </p> </td> 
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

## 屬性 {#section-50bcd15223174bb79ce08b31ea03d682}

選填。

## 預設 {#section-7564169749ff4a4996049ea1148cb2a5}

`0.5,0`

## 範例 {#section-96e69b70365f461dae4399e49044ea2f}

`transition=2,2`
