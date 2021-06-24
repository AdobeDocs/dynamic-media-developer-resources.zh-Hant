---
description: ZoomView.transition
solution: Experience Manager
title: ZoomView.transition
feature: Dynamic Media Classic，檢視器，SDK/API，縮放
role: Developer,Business Practitioner
exl-id: 3ae12e0a-0647-4cb1-9785-c854b4586c47
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 3%

---

# ZoomView.transition{#zoomview-transition}

` [ZoomView.|<containerId>_zoomView.]transition= *``*[, *`調整`*]`

<table id="table_9E7BB12BF371419F88DD4D24EF04632C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 時間</span> </span> </p> </td> 
   <td colname="col2"> <p> 指定單縮放步驟操作的動畫所花費的秒數。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 寬鬆</span> </span> </p> </td> 
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

## 屬性 {#section-50bcd15223174bb79ce08b31ea03d682}

選填。

## 預設 {#section-7564169749ff4a4996049ea1148cb2a5}

`0.5,0`

## 範例 {#section-96e69b70365f461dae4399e49044ea2f}

`transition=2,2`
